<template>
  <v-app light>
    <!-- <v-progress-linear class="progress" :indeterminate="true" height="5"></v-progress-linear> -->

    <v-progress-linear :indeterminate="true" class="ma-0" height="6"></v-progress-linear>

    <!-- <v-toolbar class="white">
      <v-toolbar-title v-text="title"></v-toolbar-title>
    </v-toolbar>-->
    <Toolbar/>

    <v-content>
      <section>
        <v-parallax :src="getImage('hero.jpeg')" height="400">
          <v-layout column align-center justify-center class="white--text">
            <img :src="getImage('vuetify.png')" alt="Vuetify.js" height="200">
            <h1 class="white--text mb-2 display-1 text-xs-center">안녕하세요 소프트웨어 캠퍼스 입니다.</h1>
            <div class="subheading mb-3 text-xs-center">Powered by Socam</div>
            <!-- <v-btn class="blue lighten-2 mt-5" dark large href="/pre-made-themes">Get Started</v-btn> -->
          </v-layout>
        </v-parallax>`
      </section>

      <section>
        <v-layout column wrap class="my-5" align-center>
          <v-flex xs12 sm4 class="my-3">
            <div class="text-xs-center">
              <h1 class="font-weight-bold display-1">모집중인 모임</h1>
              <span class="subheading">Cras facilisis mi vitae nunc</span>
            </div>
          </v-flex>

          <GroupList/>
        </v-layout>
      </section>

      <section>
        <v-parallax :src="getImage('section.jpg')" height="300">
          <v-layout column align-center justify-center>
            <div class="headline white--text mb-3 text-xs-center">소프트웨어 캠퍼스는 여러분을 응원합니다.</div>
            <em>Kick-start your application today</em>
            <v-btn class="blue lighten-2 mt-5" dark large href="/pre-made-themes">Get Started</v-btn>
          </v-layout>
        </v-parallax>
      </section>

      <section>
        <v-container grid-list-xl>
          <v-layout row wrap justify-center class="my-5">
            <v-flex xs12 sm4>
              <v-card class="elevation-0 transparent">
                <v-card-title primary-title class="layout justify-center">
                  <div class="headline">Company info</div>
                </v-card-title>
                <v-card-text>제대로된 소프트웨어 강의를 할수 있는 사람들을 육성하고, 그것을 바탕으로 건전한 개발자 생태계를 만들어 개발자들이 즐겁게 개발할 수 있는 환경을 만드는데 기여하는 커뮤니티</v-card-text>
              </v-card>
            </v-flex>
            <v-flex xs12 sm4 offset-sm1>
              <v-card class="elevation-0 transparent">
                <v-card-title primary-title class="layout justify-center">
                  <div class="headline">Contact us</div>
                </v-card-title>
                <v-card-text>Cras facilisis mi vitae nunc lobortis pharetra. Nulla volutpat tincidunt ornare.</v-card-text>
                <v-list class="transparent">
                  <v-list-tile>
                    <v-list-tile-action>
                      <v-icon class="blue--text text--lighten-2">phone</v-icon>
                    </v-list-tile-action>
                    <v-list-tile-content>
                      <v-list-tile-title>777-867-5309</v-list-tile-title>
                    </v-list-tile-content>
                  </v-list-tile>
                  <v-list-tile>
                    <v-list-tile-action>
                      <v-icon class="blue--text text--lighten-2">place</v-icon>
                    </v-list-tile-action>
                    <v-list-tile-content>
                      <v-list-tile-title>Chicago, US</v-list-tile-title>
                    </v-list-tile-content>
                  </v-list-tile>
                  <v-list-tile>
                    <v-list-tile-action>
                      <v-icon class="blue--text text--lighten-2">email</v-icon>
                    </v-list-tile-action>
                    <v-list-tile-content>
                      <v-list-tile-title>john@vuetifyjs.com</v-list-tile-title>
                    </v-list-tile-content>
                  </v-list-tile>
                </v-list>
              </v-card>
            </v-flex>
          </v-layout>
        </v-container>
      </section>

      <Footer/>
    </v-content>
  </v-app>
</template>

<script>
import Toolbar from "./../components/Toolbar";
import Footer from "./../components/Footer";
import GroupList from "./../components/GroupList";

export default {
  data: () => ({
    title: "Software Campus"
  }),
  methods: {
    getImage(img) {
      return require(`../assets/images/${img}`);
    }
  },
  components: {
    Toolbar,
    Footer,
    GroupList
  }
};
</script>

<style scoped>
.toolbar {
  /* background-color: gray !important; */
  /* opacity: 0.5;
  z-index: 1; */
}

/* .parallex {
  position: absolute;
  z-index: 0;
  width: 100%;
}

.footer {
  position: absolute;
  bottom: 0;
}

.progress {
  margin: 0;
} */
</style>
