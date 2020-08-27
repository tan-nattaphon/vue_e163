<template>
  <v-card>
    <center>
      <span style="font-size: 100px;" class="material-icons">lock</span>
      <h1>Login {{gpa}}</h1>
    </center>

    <v-card-text>
      <v-form>
        <v-text-field prepend-icon="mdi-account-circle" label="Username" v-model="user" />
        <v-text-field
          :type="showPassword ? 'text' : 'password'"
          v-model="password"
          label="Password"
          prepend-icon="mdi-lock"
          :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
          @click:append="showPassword = !showPassword"
        />
      </v-form>
    </v-card-text>
    <v-card-actions>
      <nuxt-link to="/register">
        <v-btn color="success">REGISTER</v-btn>
      </nuxt-link>
      <v-spacer></v-spacer>
      <v-btn @click="doSave" color="primary">LOGIN</v-btn>
    </v-card-actions>
  </v-card>
</template>
<script>
export default {
  name: "App",
  data() {
    return {
      showPassword: false,
      user: "",
      password: "",
      gpa: "",
    };
  },
  methods: {
    async doSave() {
      console.log("do save");
      console.log("user:", this.user);
      console.log("password:", this.password);
      //this.$router.push('/register')
      let res = await fetch("http://localhost:7001/list?user=" + this.user);
      let data = await res.json();
      console.log("data:", data.data[0].GPA);
      this.gpa = data.data[0].GPA;
    },
  },
};
</script>