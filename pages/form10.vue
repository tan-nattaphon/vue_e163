<template>
  <v-card>
    <br />
    <center>
      <font face="TH SarabunPSK" style="font-size: 15px;">ข้อ 10</font>
      <h2>ที่ตั้งจังหวัด {{province_name}}</h2>
      <v-card-text>
        <v-form>
          <v-text-field v-model="province_code" prepend-icon="mdi-account-circle" label="จังหวัด" />
        </v-form>
        <v-btn rounded color="success" dark @click="form10">ค้นหา</v-btn>
      </v-card-text>
    </center>
  </v-card>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      student: [],
      province_name: "",
      province_code: "",
    };
  },
  methods: {
    async form10() {
      console.log("Form10");
      let res = await fetch(
        "http://localhost:7001/form10?province_code=" + this.province_code
      );
      let data = await res.json();
      console.log(data.rows[0][0].province_name);
      this.province_name = data.rows[0].province_name;
    },
  },
};
</script>