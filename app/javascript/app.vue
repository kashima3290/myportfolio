<template>
  <v-app id="app">
    <v-content
        class="fill-height p-0"
        fluid
      >
      <v-img
        width="100%"
        src="https://cdn.pixabay.com/photo/2016/10/17/14/31/background-1747776_1280.jpg">
      </v-img>
    </v-content>
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
                  height="125"></v-img>
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
                  height="125"></v-img>
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
                  height="125"></v-img>
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