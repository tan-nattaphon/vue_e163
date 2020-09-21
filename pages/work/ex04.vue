<template>
  <div>
    <v-container>
      <v-row style="color: #000000">
        <v-col cols="3" md="5">
          <v-img src="/images/turn-left.png" width="40"></v-img>
        </v-col>
        <v-col cols="6" md="5" style="text-align: center;">
          <strong>
            <h3>Card Settings</h3>
          </strong>
        </v-col>
        <v-col cols="3" md="5" style="padding-left: 33px">
          <v-img src="/images/lock.png" width="50"></v-img>
        </v-col>
      </v-row>
      <div style="color: #000000; text-align: center;">
        <h1>Card 2</h1>
        <p>4586 3456 4879 7789</p>
      </div>
      <div>
        <v-card style="background: #ddfdff; height: 50px; border-radius: 50px; text-align: center;">
          <v-row style="color: #000000">
            <v-col cols="9" sm="5" style="text-align: left; padding-left: 35px;">Connections WiFi</v-col>
            <v-col cols="3" sm="5" style="margin-top: -20px;">
              <v-switch value input-value="true"></v-switch>
            </v-col>
          </v-row>
        </v-card>
      </div>
      <br />
      <div>
        <v-card style="background: #ddfdff; height: 50px; border-radius: 50px; text-align: center;">
          <v-row style="color: #000000">
            <v-col cols="9" sm="5" style="text-align: left; padding-left: 35px;">On Phones</v-col>
            <v-col cols="3" sm="5" style="margin-top: -20px;">
              <v-switch value input-value="true"></v-switch>
            </v-col>
          </v-row>
        </v-card>
      </div>
    </v-container>
    <div>
      <v-card style="background: #ff6d00;">
        <center>
          <h2>Security Settings</h2>
          <br />
          <h3>Check on file</h3>
          <br />
          <h3>Doble vercityrisons</h3>
        </center>
      </v-card>
    </div>
    <br />
    <center>
      <v-card
        style="background: #4527a0; height: 60px; width: 200px; border-radius: 50px; text-align: center;"
      >
        <h3 style="padding-top: 15px;">Delete Card 2</h3>
      </v-card>
    </center>
  </div>
</template>
<script>
export default {
  layout: "themp4",
};
</script>