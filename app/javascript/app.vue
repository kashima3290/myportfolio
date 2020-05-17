<template>
  <v-app id="app">
    <v-content
        class="fill-height p-0"
        fluid
      >
      <v-parallax
        src="https://cdn.pixabay.com/photo/2016/10/17/14/31/background-1747776_1280.jpg">
        <p class="display-4 black--text font-weight-thin">Portfolio</p>
        <v-row justify="space-around align-end mb-3">
          <v-icon color="blue-grey darken-3">mdi-domain</v-icon>

          <v-icon color="blue-grey darken-3">mdi-message-text</v-icon>

          <v-icon color="blue-grey darken-3">mdi-dialpad</v-icon>

          <v-icon color="blue-grey darken-3">mdi-email</v-icon>

          <v-icon color="blue-grey darken-3">mdi-call-split</v-icon>

          <v-icon color="blue-grey darken-2">mdi-arrow-up-bold-box-outline</v-icon>
        </v-row>
      </v-parallax>
      <!-- 自己紹介 -->
      <v-row justify="center" align-content="center" style="height: 220px;">
        <p class="display-3 black--text font-weight-thin">Introduction</p>
      </v-row>
      <div class="d-flex justify-space-around mt-10">
        <div>
          <v-img
            src="https://i.gyazo.com/ad3a231e1d20bf596af18c7679b1a07e.jpg"
            width="90%"
            class="align-center">
          </v-img>
        </div>
        <div class="mt-10">
          <p class="display-1 black--text font-weight-thin">Name: 加島 雷一騎</p>
        </div>
      </div>
      <!-- スキルセット -->
      <v-row justify="center" align-content="center" style="height: 220px;">
        <p class="display-3 black--text font-weight-thin">Skill set</p>
      </v-row>
      <v-parallax
        src="https://cdn.pixabay.com/photo/2016/10/17/14/31/background-1747781_1280.jpg">
        <div class="mx-auto">
          <p class="black--text font-italic font-weight-light display-1">HTML&CSS</p>
          <p class="black--text font-italic font-weight-light display-1">Ruby</p>
          <p class="black--text font-italic font-weight-light display-1">Ruby on Rails</p>
          <p class="black--text font-italic font-weight-light display-1">JavaScript</p>
          <p class="black--text font-italic font-weight-light display-1">Github</p>
          <p class="black--text font-italic font-weight-light display-1">AWS</p>
          <p class="black--text font-italic font-weight-light display-1">Docker</p>
        </div>
      </v-parallax>
      <!-- ポートフォリオ一覧 -->
    <v-content
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
          <v-btn x-large color="success" dark text @click="show = true">Portfolio</v-btn>
        </v-row>

      </v-fade-transition>
    </v-content>
    </v-content>
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