<template>
  <v-card color="blue" dark>
    <center>
      <br />
      <font face="TH SarabunPSK" style="font-size: 25px;">ข้อที่ 2</font>
    </center>

    <v-card-text>
      <v-form>
        <v-text-field v-model="school_id" prepend-icon="mdi-account-circle" label="รหัสสถานศึกษา" />
        <v-text-field v-model="web_url" prepend-icon="mdi-account-circle" label="URL" />
      </v-form>
    </v-card-text>

    <v-card-actions>
      <v-spacer></v-spacer>
      <v-btn rounded color="warning" dark @click="form2">ค้นหา</v-btn>
    </v-card-actions>
  </v-card>
</template>
<script>
export default {
  data() {
    return {
      school_id: "",
      web_url: "",
    };
  },
  methods: {
    async form2() {
      console.log("Success Form2");
      console.log("school_id:", this.school_id);
      //this.$router.push('/register')
      let res = await fetch(
        "http://localhost:7001/form2?school_id=" + this.school_id
      );
      let data = await res.json();
      this.school_id = data.data[0].school_id;
      this.web_url = data.data[0].web_url;
    },
  },
};
</script>