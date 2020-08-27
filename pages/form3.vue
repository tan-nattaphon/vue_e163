<template>
  <v-card color="green accent-4" dark height="400" width="500" class="teal lighten-1">
    <center>
      <v-icon size="120">store_mall_directory</v-icon>
      <br />
      <font face="TH SarabunPSK" style="font-size: 20px;">ข้อที่ 3</font>
    </center>

    <v-card-text>
      <v-form>
        <v-text-field
          v-model="student_id"
          prepend-icon="mdi-account-circle"
          label="กรุณากรอกรหัสนักศึกษา"
        />
        <v-text-field
          v-model="school_name"
          prepend-icon="mdi-account-circle"
          label="ชื่อสถานศึกษา"
        />
      </v-form>
    </v-card-text>

    <v-card-actions>
      <v-spacer></v-spacer>
      <v-btn color="primary" @click="form3">ค้นหา</v-btn>
    </v-card-actions>
  </v-card>
</template>
<script>
export default {
  data() {
    return {
      student_id: "",
      school_name: "",
    };
  },
  methods: {
    async form3() {
      console.log("form3");
      console.log("student_id:", this.student_id);
      //this.$router.push('/register')
      let res = await fetch(
        "http://localhost:7001/form3?student_id=" + this.student_id
      );
      let data = await res.json();
      this.student_id = data.data[0].student_id;
      this.school_name = data.data[0].school_name;
    },
  },
};
</script>