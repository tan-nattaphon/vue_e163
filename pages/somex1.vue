<template>
  <v-container>
    <v-form ref="form" v-model="valid" lazy-validation>
      <v-text-field v-model="school_id" :counter="10" label="school_id"></v-text-field>

      <v-text-field v-model="school_name" :counter="50" label="school_name"></v-text-field>

      <v-btn color="error" class="mr-4">Reset Form</v-btn>
    </v-form>
  </v-container>
</template>
<script>
export default {
  data: () => ({
    school_id: "",
    school_name: "",
  }),

  methods: {
    async init_load() {
      console.log("welcome");
      let res = await fetch(
        "http://localhost:7001/form1?school_id=" + this.school_id
      );
      let data = await res.json();
      console.log("data=", data.data[0].school_id);
      this.school_name = data.data[0].school_name;
      this.school_id = data.data[0].school_id;
    },
  },
  created() {
    this.init_load();
  },
};
</script>