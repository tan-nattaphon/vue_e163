<template>
  <v-container>
    <v-form ref="form" v-model="valid" lazy-validation>
      <v-text-field v-model="code" :counter="10" label="code"></v-text-field>

      <v-text-field v-model="pre_name" :counter="10" label="title"></v-text-field>

      <v-text-field v-model="first_name" :counter="10" label="Name"></v-text-field>

      <v-text-field v-model="last_name" :counter="20" label="lastname"></v-text-field>

      <v-text-field v-model="is_active" :counter="10" label="สถานะ"></v-text-field>

      <v-btn color="error" class="mr-4">Reset Form</v-btn>

      <v-btn color="primary" @click="saveStd">Save</v-btn>
    </v-form>
  </v-container>
</template>
<script>
export default {
  data: () => ({
    code: "",
    pre_name: "",
    first_name: "",
    last_name: "",
    is_active: "",
    student: [],
  }),
  async created() {
    console.log("code_edit=", this.$route.query.code);
    let code = this.$route.query.code;
    let res = await fetch("http://localhost:7001/editstd?code=" + code);
    let data = await res.json();
    console.log("data", data);
    this.code = data.rows[0].code;
    this.pre_name = data.rows[0].pre_name;
    this.first_name = data.rows[0].first_name;
    this.last_name = data.rows[0].last_name;
    this.is_active = data.rows[0].is_active;
  },
  methods: {
    async submit() {
      let res = await fetch(
        "http://localhost:7001/insert?code=" +
          this.code +
          "&pre_name=" +
          this.pre_name +
          "&first_name=" +
          this.first_name +
          "&last_name=" +
          this.last_name +
          "&is_active=" +
          this.is_active
      );
      let data = await res.json();
    },
    async saveStd() {
      console.log("saveStd");
      let student = {
        code: this.code,
        pre_name: this.pre_name,
        first_name: this.first_name,
        last_name: this.last_name,
        is_active: this.is_active,
      };
      let res = await this.$http.post("http://localhost:7001/addstd2", student);
      // let data = await res.json()
      console.log("row=", res.data.rows);
    },
    clear() {
      this.code = "";
      this.pre_name = "";
      this.first_name = "";
      this.last_name = "";
      this.is_active = "";
    },
  },
};
</script>