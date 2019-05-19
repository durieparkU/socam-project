<template>
  <v-app light>
    <v-progress-linear :indeterminate="true" class="ma-0" height="6"></v-progress-linear>
    <Toolbar/>
    <v-content>
      <section>
        This is a about page
      </section>
    </v-content>
    <Footer/>
  </v-app>
</template>

<script>
import Toolbar from "./../components/Toolbar";
import Footer from "./../components/Footer";

export default {
  data() {
    return {};
  },
  components: {
    Toolbar,
    Footer
  }
};
</script>

