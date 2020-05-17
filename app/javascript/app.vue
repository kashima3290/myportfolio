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
        <!-- 右 -->
        <div>
          <v-card
            class="mx-auto"
            max-width="100%"
            height="550px"
            tile
          >
            <v-list-item>
              <v-list-item-content>
                <v-list-item-title>加島雷一騎</v-list-item-title>
                <v-list-item-subtitle>20歳&emsp;大阪&emsp;大学3回生</v-list-item-subtitle>
              </v-list-item-content>
            </v-list-item>

            <v-list-item two-line>
              <v-list-item-content>
                <v-list-item-title>学歴</v-list-item-title>
                <v-list-item-subtitle>2018年4月&emsp;佛教大学社会福祉学部入学</v-list-item-subtitle>
                <v-list-item-subtitle>2020年3月&emsp;短期集中プログラミングスクール TECH::CAMP（株式会社div）</v-list-item-subtitle>
              </v-list-item-content>
            </v-list-item>

            <v-list-item three-line>
              <v-list-item-content>
                <p class="text-justify">
                  大学生活の中でプログラミングでのものづくりによって人を笑顔にすることに興味を持ち、プログラミングスクールにいくことを決断しました。<br><br>卒業した後も、日々新しい技術を勉強しています。<br>主な言語は HTML&CSS・Ruby・Ruby on Rails・JavaScript・Githubを学び、バックエンドに力を注いでいます。<br><br>現在は現場での経験を積みたい一心で、インターン先を探しています。採用されたからには必ず役に立てるよう努力しますので、よろしくお願いします。<br><br>Ruby on Railsでのチーム開発の経験から、共に成長しあえる関係性を学び、<br>誰かと共に開発に携わりたいという思いがあります。<br>またその中で、新たに成長しあえる関係を生み出していきたいです。
                </p>
              </v-list-item-content>
            </v-list-item>
          </v-card>
        </div>
      </div>
      <!-- スキルセット -->
      <v-row justify="center" align-content="center" style="height: 220px;">
        <p class="display-3 black--text font-weight-thin">Skill set</p>
      </v-row>
      <v-parallax
        src="https://cdn.pixabay.com/photo/2016/10/17/14/31/background-1747781_1280.jpg">
        <div class="mx-auto">
          <div class="d-flex  mb-4">
            <v-icon color="yellow darken-3" large>mdi-language-html5</v-icon>&emsp;
            <p class="black--text font-italic font-weight-light display-1 mb-0">HTML&CSS</p>
          </div>

          <div class="d-flex mb-4">
            <v-icon color="red darken-3" large>mdi-ruby</v-icon>&emsp;
            <p class="black--text font-italic font-weight-light display-1 mb-0">Ruby</p>
          </div>

          <div class="d-flex mb-4">
            <v-icon color="red darken-3" large>mdi-language-ruby-on-rails</v-icon>&emsp;
            <p class="black--text font-italic font-weight-light display-1 mb-0">Ruby on Rails</p>
          </div>

          <div class="d-flex mb-4">
            <v-icon color="yellow darken-3" dark large>mdi-language-javascript</v-icon>&emsp;
            <p class="black--text font-italic font-weight-light display-1 mb-0">JavaScript</p>
          </div>

          <div class="d-flex mb-4">
            <v-icon color="blue-grey darken-3" large>mdi-git</v-icon>&emsp;
            <p class="black--text font-italic font-weight-light display-1 mb-0">Github</p>
          </div>

          <div class="d-flex mb-4">
            <v-icon color="orange darken-3" large>mdi-aws</v-icon>&emsp;
            <p class="black--text font-italic font-weight-light display-1 mb-0">AWS</p>
          </div>

          <div class="d-flex mb-4">
            <v-icon color="blue darken-3" large>mdi-docker</v-icon>&emsp;
            <p class="black--text font-italic font-weight-light display-1 mb-0">Docker</p>
          </div>

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
                  height="300"></v-img>
                  <v-card-title class="title">Line Bot</v-card-title>
                  <v-fade-transition>
                    <v-overlay
                      v-if="hover"
                      absolute
                      color="#036358"
                    >
                      <v-btn href="https://i.gyazo.com/2d19c78708f97ba31c4dbc8aaa1d17fa.png">Go to app</v-btn>
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
                  height="300"></v-img>
                  <v-card-title class="title">Hash Literal</v-card-title>
                  <v-fade-transition>
                    <v-overlay
                      v-if="hover"
                      absolute
                      color="#036358"
                    >
                      <v-btn href="http://www.hash-literal.com/">Go to app</v-btn>
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
                  height="300"></v-img>
                  <v-card-title class="title">meetup</v-card-title>
                  <v-fade-transition>
                    <v-overlay
                      v-if="hover"
                      absolute
                      color="#036358"
                    >
                      <v-btn href="http://18.180.202.49/">Go to app</v-btn>
                    </v-overlay>
                  </v-fade-transition>
                </v-card>
              </v-col>
            </template>
          </v-hover>
          <!-- Github -->
          <v-hover>
            <template v-slot:default="{ hover }">
              <v-col cols="6">
                <v-card>
                  <v-img src="https://i.gyazo.com/794a57a42a65c421e8f6609c9a0e0bb2.png"
                  height="300"></v-img>
                  <v-card-title class="title">Github</v-card-title>
                  <v-fade-transition>
                    <v-overlay
                      v-if="hover"
                      absolute
                      color="#036358"
                    >
                      <v-btn href="https://github.com/kashima3290">Go to site</v-btn>
                    </v-overlay>
                  </v-fade-transition>
                </v-card>
              </v-col>
            </template>
          </v-hover>
        </v-row>
        <v-row v-else key="1" justify="center">
          <v-btn class="my-10" height="100px" width="200px" x-large color="success" dark rounded @click="show = true">Portfolio</v-btn>
        </v-row>

      </v-fade-transition>
    </v-content>
    <!-- 連絡先 -->
      <v-row justify="center" align-content="center" style="height: 320px;">
          <p class="display-3 black--text font-weight-thin">Contact</p>
      </v-row>
      <v-parallax
        height="300"
        src="https://cdn.pixabay.com/photo/2017/07/09/13/01/white-2486923_1280.jpg"
      >
        <div class="d-flex justify-space-around mt-10">
          <div class="mt-10 black--text black--text font-weight-thin headline">
            <p class="my-10 black--text black--text font-weight-thin headline">phone number</p>
            <p class="my-10 black--text black--text font-weight-thin headline">email</p>
          </div>
          <div class="mt-10 black--text black--text font-weight-thin headline">
            <p class="my-10 black--text black--text font-weight-thin headline">080-2472-1832</p>
            <p class="my-10 black--text black--text font-weight-thin headline">raiki3290@gmail.com</p>
          </div>
        </div>
      </v-parallax>
      <!-- フッター -->
      <v-footer
        gray
        dark
      >
        <v-card
          class="flex"
          gray
          dark
        >
          <v-card-title class="gray">
            <strong class="subheading">Please Follow me if you like!</strong>

            <v-spacer></v-spacer>

            <v-btn
              class="mx-4"
              dark
              icon
              href="https://twitter.com/raiki3232"
            >
              <v-icon size="24px">mdi-twitter</v-icon>
            </v-btn>
            <v-btn
              class="mx-4"
              dark
              icon
              href="https://www.instagram.com/raiki_3"
            >
              <v-icon size="24px">mdi-instagram</v-icon>
            </v-btn>
            <v-btn
              class="mx-4"
              dark
              icon
              href="https://www.wantedly.com/users/130702131"
            >
              <v-icon size="24px">mdi-alpha-w-box-outline</v-icon>
            </v-btn>
            <v-btn
              class="mx-4"
              dark
              icon
              href="https://line.me/ti/p/fXlCf5Fbdy"
            >
              <v-icon>fab fa-line</v-icon>
            </v-btn>
          </v-card-title>

        </v-card>
      </v-footer>
    </v-content>
  </v-app>
</template>

<script>
import Header from "./components/Header";

export default {
  data: function () {
    return {
      show: false,
      icons: [
        'mdi-facebook',
        'mdi-twitter',
        'mdi-linkedin',
        'mdi-instagram',
      ],
    }
  },
  components: {
    Header,
  }
}
</script>