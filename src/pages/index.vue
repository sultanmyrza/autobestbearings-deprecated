<template>
  <v-layout column justify-center align-center>
    <v-flex xs12 sm8 md6>
      <div class="text-center"></div>
      <v-card class="mx-auto">
        <v-card-title class="headline">
          Welcome to Auto Best Bearings
        </v-card-title>
        <v-card-text class="text--primary">
          <div>The first brand of automative bearings</div>
        </v-card-text>
        <v-img
          class="white--text align-end"
          src="http://autobestbearings.com/images/home-pic.jpg"
          gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
        >
          <v-card-title> AUTO BEST BEARINGS CO., LTD</v-card-title>
        </v-img>
        <v-card-actions>
          <v-btn :to="'about'" color="orange" text>
            more
          </v-btn>

          <v-btn :to="'products'" color="orange" text>
            products
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
export default {}
</script>
