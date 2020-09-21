<template>
  <div>
    <v-container>
      <v-row style="color: #000000">
        <v-col cols="3" md="5">
          <v-img src="/images/turn-left.png" width="40"></v-img>
        </v-col>
        <v-col cols="6" md="5" style="text-align: center;">
          <h2>Card 2</h2>
          <p>about join add job</p>
        </v-col>
        <v-col cols="3" md="5" style="padding-left: 33px">
          <v-img src="/images/lock.png" width="50"></v-img>
        </v-col>
      </v-row>
      <div style="color: #000000; text-align: center;">
        <h1 style="font-size: 40px">70, 05 USD</h1>
        <p>Active Pororce</p>
      </div>
      <v-row>
        <v-col cols="6" md="5">
          <v-card
            style="background: #ff6d00; height: 55px; border-radius: 50px; text-align: center;"
          >
            <h3 style="padding-top: 15px;">Send</h3>
          </v-card>
        </v-col>
        <v-col cols="6" md="5">
          <v-card
            style="background: #6340ce; height: 55px; border-radius: 50px; text-align: center;"
          >
            <h3 style="padding-top: 15px;">Settings</h3>
          </v-card>
        </v-col>
      </v-row>
      <div>
        <v-card
          style="background: #6340ce; height: 30px; width: 90px; border-radius: 50px; text-align: center;"
        >
          <p style="font-size: 12px; padding-top: 6px;">10/09/2000</p>
        </v-card>
        <div style="color: #000000;">
          <v-row>
            <v-col cols="6" sm="5" style="text-align: left;">
              <p>Taxl</p>
            </v-col>
            <v-col cols="6" sm="5" style="text-align: right;">
              <p style="color: red;">- 20 USB</p>
            </v-col>
          </v-row>
          <hr />
          <v-row>
            <v-col cols="6" sm="5" style="text-align: left;">
              <p>Poynement</p>
            </v-col>
            <v-col cols="6" sm="5" style="text-align: right;">
              <p style="color: green;">+ 300 USB</p>
            </v-col>
          </v-row>
          <hr />
          <v-row>
            <v-col cols="6" sm="5" style="text-align: left;">
              <p>Bonney</p>
            </v-col>
            <v-col cols="6" sm="5" style="text-align: right;">
              <p style="color: red;">- 40, 28 USB</p>
            </v-col>
          </v-row>
          <hr />
        </div>
      </div>
    </v-container>
  </div>
</template>
<script>
export default {
  layout: "themp3",
};
</script>