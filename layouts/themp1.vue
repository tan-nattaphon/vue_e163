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
    <v-content>
      <v-container>
        <!-- เนื้อหา -->
        <nuxt />
      </v-container>
    </v-content>
  </v-app>
</template>

<style scoped>
.bg1 {
  background: #4527a0;
}
</style>