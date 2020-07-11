<template>
  <v-container fluid class="pa-0">
    <v-row align="center">
      <v-col cols="12" sm="6">
        <div class="text-center">
          <div class="my-2">
            <nuxt-link to="/activity/flag"><v-btn width="50%" color="secondary" dark>กิจกรรมหน้าเสาธง</v-btn></nuxt-link> 
          </div>
          <div class="my-2">
            <nuxt-link to="/activity/homeroom"><v-btn width="50%" color="primary" dark>กิจกรรม Homeroom</v-btn></nuxt-link>
          </div>
          <div class="my-2">
            <nuxt-link to="/activity/extra"><v-btn width="50%" color="warning" dark>กิจกรรมพิเศษ</v-btn></nuxt-link>
          </div>
          <div class="my-2">
            <nuxt-link to="/activity/profession"><v-btn width="50%" color="error" dark>กิจกรรมวิชาชีพ</v-btn></nuxt-link>
          </div>
          <div class="my-2">
            <nuxt-link to="/"><v-btn x-large color="success" dark>กลับมาหน้าหลัก</v-btn></nuxt-link>
          </div>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>