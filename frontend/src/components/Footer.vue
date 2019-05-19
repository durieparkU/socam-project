<template>
  <section>
    <v-footer dark height="auto">
      <v-card class="flex" flat tile>
        <v-card-title class="primary lighten-1">
          <strong class="subheading">Get connected with us on social networks!</strong>

          <v-spacer></v-spacer>

          <v-btn v-for="icon in icons" :key="icon" class="mx-3" dark icon>
            <v-icon size="24px">{{ icon }}</v-icon>
          </v-btn>
        </v-card-title>

        <v-card-actions class="grey darken-3 justify-center">
          &copy;2018 —
          <strong>Vuetify</strong>
        </v-card-actions>
      </v-card>
    </v-footer>

    <!-- <v-footer class="footer" dark>
      <v-card flat tile class="indigo lighten-1 white--text text-xs-center">
        <v-card-text>
          <v-btn v-for="icon in icons" :key="icon" class="mx-3 white--text" icon>
            <v-icon size="24px">{{icon}}</v-icon>
          </v-btn>
        </v-card-text>

        <v-card-text
          class="white--text pt-0"
        >Phasellus feugiat arcu sapien, et iaculis ipsum elementum sit amet. Mauris cursus commodo interdum. Praesent ut risus eget metus luctus accumsan id ultrices nunc. Sed at orci sed massa consectetur dignissim a sit amet dui. Duis commodo vitae velit et faucibus. Morbi vehicula lacinia malesuada. Nulla placerat augue vel ipsum ultrices, cursus iaculis dui sollicitudin. Vestibulum eu ipsum vel diam elementum tempor vel ut orci. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.</v-card-text>

        <v-divider></v-divider>

        <v-card-text class="white--text">
          &copy;2018 —
          <strong>Vuetify</strong>
        </v-card-text>
      </v-card>
    </v-footer>-->
    <!-- <v-footer class="blue darken-2">
          <v-layout row wrap align-center>
            <v-flex xs12>
              <div class="white--text ml-3">
                Made with
                <v-icon class="red--text">favorite</v-icon>
                by <a class="white--text" href="https://vuetifyjs.com" target="_blank">Vuetify</a>
                and <a class="white--text" href="https://github.com/vwxyzjn">Costa Huang</a>
              </div>
            </v-flex>
          </v-layout>
    </v-footer>-->
  </section>
</template>

<script>
export default {
  data: function() {
    return {
      icons: [
        "fa fa-facebook-official",
        "fa fa-google-plus-square",
        "fa fa-instagram"
      ]
    };
  },
  methods: {}
};
</script>

