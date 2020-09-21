<template>
  <div style="text-align: center;">
    <v-container>
      <v-row>
        <v-col cols="6" md="8">
          <v-img src="/images/avatar.png"></v-img>
        </v-col>
        <v-col cols="6" md="8" style="text-align: left; ">
          <h2>Name</h2>
          <h2 style="margin-top: -10px;">Sumame</h2>
          <p style="padding-top: 15px;">Photo Number</p>
          <p style="margin-top: -20px;">+7 587 456 25 66</p>
          <v-row style="margin-top: -20px;">
            <v-col cols="4" md="4">
              <v-img src="/images/edit.png" width="30px"></v-img>
            </v-col>
            <v-col cols="4" md="4">
              <v-img src="/images/po.png" width="30px"></v-img>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
    <div>
      <v-card class="bgex02">
        <v-container>
          <div>
            <v-row>
              <v-col cols="9" md="4">
                <h2 style="text-align: left;">Your Cards</h2>
              </v-col>
              <v-col cols="3" md="4">
                <v-img src="/images/+.png" width="40"></v-img>
              </v-col>
            </v-row>
            <v-card
              style="background: #ff6d00; height: 70px; border-radius: 50px; margin-left: -45px;"
            >
              <v-row>
                <v-col cols="6" md="8">
                  <h2>Card 1</h2>
                </v-col>
                <v-col cols="6" md="8">
                  <h3>150, 05</h3>
                  <h3>USD</h3>
                </v-col>
              </v-row>
            </v-card>
            <br />
            <v-card
              style="background: #6340ce; height: 70px; border-radius: 50px; margin-left: -45px;"
            >
              <v-row>
                <v-col cols="6" md="8">
                  <h2>Card 2</h2>
                </v-col>
                <v-col cols="6" md="8">
                  <h3>70, 05</h3>
                  <h3>USD</h3>
                </v-col>
              </v-row>
            </v-card>
            <br />
            <v-card
              style="background: #fc862e; height: 70px; border-radius: 50px; margin-left: -45px;"
            >
              <v-row>
                <v-col cols="6" md="8">
                  <h2>Card 2</h2>
                </v-col>
                <v-col cols="6" md="8">
                  <h3>2000, 05</h3>
                  <h3>USD</h3>
                </v-col>
              </v-row>
            </v-card>
          </div>
        </v-container>
      </v-card>
    </div>
  </div>
</template>
<style scoped>
.bgex02 {
  background: #ffffff;
  color: #000000;
  height: 350px;
}
</style>
<script>
export default {
  layout: "themp2",
};
</script>