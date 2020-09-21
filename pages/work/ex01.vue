<template>
  <div style="text-align: center;">
    <v-container>
      <v-img class="img-logo" src="../images/logo_work.png" width="130"></v-img>
      <h1>Your Bank</h1>
      <br />
      <center>
        <v-form>
          <v-text-field
            label="Username"
            outlined
            v-model="user"
            style="width: 240px; border-radius: 30px;"
          />
          <v-text-field
            :type="showPassword ? 'text' : 'password'"
            v-model="password"
            label="Password"
            :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
            @click:append="showPassword = !showPassword"
            outlined
            style="width: 240px; border-radius: 30px;"
          />
        </v-form>
      </center>
      <v-btn
        style="font-size: 18px; width: 240px; height: 40px; border-radius: 20px;"
        color="#FF6D00"
      >Sign Up</v-btn>
    </v-container>
  </div>
</template>

<style scoped>
.img-logo {
  margin-left: auto;
  margin-right: auto;
  margin-top: 60px;
}
h1 {
  text-align: center;
  text-shadow: 2px 2px #696c6d;
  font-size: 45px;
}
</style>

<script>
export default {
  layout: "themp1",
  data() {
    return {
      showPassword: false,
    };
  },
};
</script>