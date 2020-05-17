<template>
  <v-app id="app">
    <v-content
        class="fill-height p-0"
        fluid
      >
      <v-parallax
        src="https://cdn.pixabay.com/photo/2016/10/17/14/31/background-1747776_1280.jpg">
        <p class="display-4 black--text font-weight-thin">Portfolio</p>
        <v-row justify="space-around">
          <v-icon large color="green darken-2">mdi-domain</v-icon>

          <v-icon large color="blue darken-2">mdi-message-text</v-icon>

          <v-icon large color="purple darken-2">mdi-dialpad</v-icon>

          <v-icon large color="teal darken-2">mdi-email</v-icon>

          <v-icon large color="blue-grey darken-2">mdi-call-split</v-icon>

          <v-icon large color="orange darken-2">mdi-arrow-up-bold-box-outline</v-icon>
        </v-row>
      </v-parallax>
    </v-content>
    <!-- 自己紹介 -->
    <!-- ポートフォリオ一覧 -->
    <v-container
      class="fill-height"
      fluid
      style="min-height: 434px"
    >
      <v-fade-transition mode="out-in">
        <v-row v-if="show" key="0">

          <!-- Weather Bot -->
          <v-hover>
            <template v-slot:default="{ hover }">
              <v-col cols="6">
                <v-card>
                  <v-img src="https://i.gyazo.com/9f006436148805e45172639c7ae55d02.png"
                  height="200"></v-img>
                  <v-card-title class="title">Line Bot</v-card-title>
                  <v-fade-transition>
                    <v-overlay
                      v-if="hover"
                      absolute
                      color="#036358"
                    >
                      <v-btn>Go to app</v-btn>
                    </v-overlay>
                  </v-fade-transition>
                </v-card>
              </v-col>
            </template>
          </v-hover>

          <!-- Hash litelal -->
          <v-hover>
            <template v-slot:default="{ hover }">
              <v-col cols="6">
                <v-card>
                  <v-img src="https://i.gyazo.com/e50e15b4c84028124ee3dfb7d0da6f6a.jpg"
                  height="200"></v-img>
                  <v-card-title class="title">Hash Literal</v-card-title>
                  <v-fade-transition>
                    <v-overlay
                      v-if="hover"
                      absolute
                      color="#036358"
                    >
                      <v-btn>Go to app</v-btn>
                    </v-overlay>
                  </v-fade-transition>
                </v-card>
              </v-col>
            </template>
          </v-hover>

          <!-- meetup -->
          <v-hover>
            <template v-slot:default="{ hover }">
              <v-col cols="6">
                <v-card>
                  <v-img src="https://i.gyazo.com/25576e7ba493c6ea751d4ade86c35c78.jpg"
                  height="200"></v-img>
                  <v-card-title class="title">meetup</v-card-title>
                  <v-fade-transition>
                    <v-overlay
                      v-if="hover"
                      absolute
                      color="#036358"
                    >
                      <v-btn>Go to app</v-btn>
                    </v-overlay>
                  </v-fade-transition>
                </v-card>
              </v-col>
            </template>
          </v-hover>

        </v-row>

        <v-row v-else key="1" justify="center">
          <v-btn text @click="show = true">Portfolio</v-btn>
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