<template>
  <div>
    <div>
      <h1>Student List</h1>
      <ul>
        <li v-for="std in student" :key="std.code">
          <span>{{ std.code }}</span>
          <span>{{ std.pre_name }}</span>
          <span>{{ std.first_name }}</span>
          <span>{{ std.last_name }}</span>
          <span>{{ std.is_active }}</span>
          <v-btn @click="edit(std.code)">EDIT</v-btn>
          <v-btn @click="del(std.code)">DEL</v-btn>
        </li>
      </ul>
    </div>
    <v-btn @click="listStd">Click</v-btn>
  </div>
</template>

<script>
export default {
  data() {
    return {
      headers: [
        {
          text: "รหัส",
          align: "start",
          sortable: false,
          value: "code",
        },
        { text: "คำนำหน้า", value: "pre_name" },
        { text: "ชื่อ", value: "first_name" },
        { text: "สกุล", value: "last_name" },
        { text: "สถานะ", value: "is_active" },
      ],
      student: [],
    };
  },
  created() {
    this.listStd();
  },
  methods: {
    async listStd() {
      console.log("List Success");
      let res = await fetch("http://localhost:7001/listStd");
      let data = await res.json();
      console.log("data", data);
      this.student = data.rows;
    },
    edit(code) {
      console.log("code=", code);
      this.$router.push("list_edit3_std?code=" + code);
    },
    async del(code) {
      console.log("code=", code);
      let res = await this.$http.post("http://localhost:7001/del?code=" + code);
      // this.$router.push("list_edit3_std?code=" + code);
    },
  },
};
</script>