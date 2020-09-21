<template>
  <v-app class="bg1">
    <div>
      <v-system-bar color="deep-purple darken-3">
        <v-spacer></v-spacer>
        <v-icon>mdi-wifi-strength-4</v-icon>
        <v-icon>mdi-signal-cellular-outline</v-icon>
        <v-icon>mdi-battery</v-icon>
        <span>12:30</span>
      </v-system-bar>
    </div>
    <div>
      <v-app-bar color="deep-purple darken-3" dense dark style="color: #000000; border-color: red;">
        <v-app-bar-nav-icon></v-app-bar-nav-icon>
        <v-spacer></v-spacer>
        <v-btn icon style="width: 25px; padding-right: 20px;">
          <v-img src="/images/Alert_white.png"></v-img>
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
.bg1 {
  background: #ffffff;
}
</style>