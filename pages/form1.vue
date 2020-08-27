<template>
  <v-card color="blue" dark>
    <center>
      <br />
      <font face="TH SarabunPSK" style="font-size: 25px;">ข้อที่ 1</font>
    </center>

    <v-card-text>
      <v-form>
        <v-text-field v-model="school_id" prepend-icon="mdi-account-circle" label="รหัสสถานศึกษา" />
        <v-text-field
          v-model="school_name"
          prepend-icon="mdi-account-circle"
          label="ชื่อสถานศึกษา"
        />
      </v-form>
    </v-card-text>

    <v-card-actions>
      <v-spacer></v-spacer>
      <v-btn rounded color="warning" dark @click="form1">ค้นหา</v-btn>
    </v-card-actions>
  </v-card>
</template>
<script>
export default {
  data() {
    return {
      school_id: "",
      school_name: "",
    };
  },
  methods: {
    async form1() {
      console.log("Success Form1");
      console.log("user:", this.school_id);
      //this.$router.push('/register')
      let res = await fetch(
        "http://localhost:7001/form1?school_id=" + this.school_id
      );
      let data = await res.json();
      this.school_id = data.data[0].school_id;
      this.school_name = data.data[0].school_name;
    },
  },
};
</script>