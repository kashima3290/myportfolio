<template>
  <v-app id="app">
    <v-container
      class="fill-height"
      fluid
      style="min-height: 434px"
    >
      <v-fade-transition mode="out-in">
        <v-row v-if="show" key="0">
          <v-col cols="6">
            <v-card>
              <v-img
                src="https://cdn.pixabay.com/photo/2016/10/17/14/31/background-1747781_1280.jpg"
                height="125"
                class="grey darken-4"
              ></v-img>
              <v-card-title class="title">height</v-card-title>
            </v-card>
          </v-col>

          <v-col cols="6">
            <v-card>
              <v-img
                src="https://cdn.pixabay.com/photo/2016/10/17/14/31/background-1747781_1280.jpg"
                height="125"
                contain
                class="grey darken-4"
              ></v-img>
              <v-card-title class="title">height with contain</v-card-title>
            </v-card>
          </v-col>

          <v-col cols="6">
            <v-card>
              <v-img
                src="https://cdn.pixabay.com/photo/2016/10/17/14/31/background-1747781_1280.jpg"
                max-height="125"
                class="grey darken-4"
              ></v-img>
              <v-card-title class="title">max-height</v-card-title>
            </v-card>
          </v-col>

          <v-col cols="6">
            <v-card>
              <v-img
                src="/assets/portfolio1.jpg"
                max-height="125"
                contain
                class="grey darken-4"
              ></v-img>
              <v-card-title class="title">max-height with contain</v-card-title>
            </v-card>
          </v-col>
        </v-row>

        <v-row v-else key="1" justify="center">
          <v-btn text @click="show = true">Load images</v-btn>
        </v-row>
      </v-fade-transition>
    </v-container>
  </v-app>
</template>

<script>
import Header from "./components/Header";

export default {
  data: function () {
    return {
      show: false,
    }
  },
  components: {
    Header,
  }
}
</script>