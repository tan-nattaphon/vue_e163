<template>
  <v-app class="bg">
    <div>
      <v-system-bar dark color="white"></v-system-bar>
      <v-app-bar color="white" dense dark style="color: #000000; border-color: red;">
        <v-app-bar-nav-icon style="color: #000000"></v-app-bar-nav-icon>
        <v-spacer></v-spacer>
        <v-btn icon style="width: 25px; padding-right: 20px;">
          <v-img src="/images/Alert.png"></v-img>
        </v-btn>
      </v-app-bar>
    </div>
    <v-content>
      <!-- เนื้อหา -->
      <nuxt />
    </v-content>
  </v-app>
</template>
<style scoped>
.bg {
  background: #4527a0;
}
</style>