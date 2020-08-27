<template>
  <v-data-table :headers="headers" :items="student" :items-per-page="5" class="elevation-1"></v-data-table>
</template>

<script>
export default {
  data() {
    return {
      headers: [
        {
          text: "CODE",
          align: "start",
          sortable: false,
          value: "code",
        },
        { text: "ชื่อ", value: "first_name" },
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
      console.log("list std");
      let res = await fetch("http://localhost:7001/listStd");
      let data = await res.json();
      console.log("data", data.rows);
      this.student = data.rows[0];
    },
  },
};
</script>