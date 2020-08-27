<template>
  <v-card>
    <br />
    <center>
      <font face="TH SarabunPSK" style="font-size: 15px;">ข้อ 5</font>
      <v-card-text>
        <v-form>
          <v-text-field
            v-model="school_id"
            prepend-icon="mdi-account-circle"
            label="รหัสสถานศึกษา"
          />
          <v-text-field v-model="gpa" prepend-icon="mdi-account-circle" label="GPA" />
        </v-form>
        <v-btn rounded color="success" dark @click="form5">ค้นหา</v-btn>
        <v-data-table :headers="headers" :items="student" :items-per-page="5" class="elevation-1"></v-data-table>
      </v-card-text>
    </center>
  </v-card>
</template>

<script>
export default {
  name: "App",
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
        { text: "ชื่อสถาศึกษา", value: "school_name" },
        { text: "GPA", value: "GPA" },
      ],
      student: [],
      school_id: "",
      gpa: "",
    };
  },
  methods: {
    async form5() {
      console.log("Form5");
      let res = await fetch(
        "http://localhost:7001/form5?school_id=" +
          this.school_id +
          "&gpa=" +
          this.gpa
      );
      let data = await res.json();
      console.log("data", data.data[0]);
      this.student = data.data[0];
    },
  },
};
</script>