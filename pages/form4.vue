<template>
  <v-card>
    <v-form>
      <v-text-field v-model="school_id" prepend-icon="mdi-account-circle" label="รหัสสถานศึกษา" />
    </v-form>
    <center>
      <v-btn color="primary" @click="form4">ค้นหา</v-btn>
    </center>
    <h1>Student List</h1>
    <v-data-table :headers="headers" :items="student" :items-per-page="5" class="elevation-1"></v-data-table>
  </v-card>
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
      school_id: "",
    };
  },
  methods: {
    async form4() {
      console.log("list");
      let res = await fetch(
        "http://localhost:7001/form4?school_id=" + this.school_id
      );
      let data = await res.json();
      console.log("data", data.data[0]);
      this.student = data.data[0];
    },
  },
};
</script>