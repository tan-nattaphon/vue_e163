<template>
  <div>
    <h1>Student List</h1>
    <v-data-table :headers="headers" :items="student" :items-per-page="5" class="elevation-1"></v-data-table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      headers: [
        {
          text: "รหัสนักศึกษา",
          align: "start",
          sortable: false,
          value: "student_id",
        },
        { text: "ชื่อ", value: "name" },
        { text: "นามสกุล", value: "lastname" },
        { text: "GPA", value: "GPA" },
      ],
      student: [],
    };
  },
  created() {
    this.listStudent();
  },
  methods: {
    async listStudent() {
      console.log("list std");
      let res = await fetch("http://localhost:7001/listStd1");
      let data = await res.json();
      console.log("data", data.data[0]);
      this.student = data.data[0];
    },
  },
};
</script>