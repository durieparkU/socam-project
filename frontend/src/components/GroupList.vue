<template>
  <v-flex xs12>
    <v-container grid-list-xl>
      <v-layout row wrap align-center>
        <v-flex xs12 sm4 v-for="(card,index) in cards" :key="index">
          <v-hover>
            <v-card
              slot-scope="{ hover }"
              :class="`elevation-${hover ? 12 : 2}`"
              class="study-card mx-auto"
              to="/about"
            >
              <v-img height="150px" :src="card.src" :aspect-ratio="16/9">
                <!-- <v-container fill-height fluid>
                          <v-layout fill-height>
                            <v-flex xs12 align-end flexbox>
                              <span class="headline">{{card.title}}</span>
                            </v-flex>
                          </v-layout>
                </v-container>-->
                <v-expand-transition>
                  <div
                    v-if="hover"
                    class="d-flex transition-fast-in-fast-out orange darken-2 v-card--reveal display-3 white--text"
                    style="height: 100%;"
                  >
                    <!-- <v-btn absolute color="orange" class="white--text" fab large >
                              <v-icon>mdi-cart</v-icon>
                    </v-btn>-->
                  </div>
                </v-expand-transition>
              </v-img>
              <v-card-title>
                <div>
                  <span class="headline black--text font-weight-medium">{{card.title}}</span>
                  <br>
                  <span>{{card.desc}}</span>
                  <!-- <br>
                  <span>Whitsunday Island, Whitsunday Islands</span>-->
                </div>
              </v-card-title>
              <v-card-actions>
                <v-list-tile class="grow">
                  <v-list-tile-avatar color="grey darken-3">
                    <v-img class="elevation-6" :src="card.userImg"></v-img>
                  </v-list-tile-avatar>

                  <v-list-tile-content>
                    <v-list-tile-title>{{card.founder}}</v-list-tile-title>
                  </v-list-tile-content>

                  <v-layout align-center justify-end>
                    <!-- <v-icon class="mr-1">mdi-heart</v-icon> -->
                    <!-- <span class="">모집중</span> -->
                    <!-- <span class="mr-1">·</span> -->
                    <!-- <v-icon class="mr-1">mdi-share-variant</v-icon> -->
                    <!-- <span class="subheading">45</span> -->
                  </v-layout>
                </v-list-tile>
              </v-card-actions>
            </v-card>
          </v-hover>
        </v-flex>

        <!-- <v-flex xs12 md4>
                  <v-card class="elevation-0 transparent">
                    <v-card-text class="text-xs-center">
                      <v-icon x-large class="blue--text text--lighten-2">color_lens</v-icon>
                    </v-card-text>
                    <v-card-title primary-title class="layout justify-center">
                      <div class="headline text-xs-center">Tensoflow 2.0</div>
                    </v-card-title>
                    <v-card-text>
                      Cras facilisis mi vitae nunc lobortis pharetra. Nulla volutpat tincidunt ornare. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Nullam in aliquet odio. Aliquam eu est vitae tellus bibendum tincidunt. Suspendisse
                      potenti.
                    </v-card-text>
                  </v-card>
        </v-flex>-->
      </v-layout>
    </v-container>
  </v-flex>
</template>

<script>
import { CARDS } from "./mock-data/mock-cards.js";

export default {
  data() {
    return {
      cards: CARDS
    };
  }
};
</script>

<style scoped>
.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: 0.5;
  position: absolute;
  width: 100%;
}

.study-card {
  cursor: pointer;
}
</style>


