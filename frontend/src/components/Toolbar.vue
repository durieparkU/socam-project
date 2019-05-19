<template>
  <!-- <v-toolbar class="toolbar" dark extended> -->
    <!-- <v-progress-linear :indeterminate="true" class="ma-0" height="6"></v-progress-linear> -->
    <v-toolbar class="toolbar" extended>
      <!-- <v-toolbar-side-icon></v-toolbar-side-icon> -->
      <v-avatar color="grey lighten-4">
        <img src="https://vuetifyjs.com/apple-touch-icon-180x180.png" alt="avatar">
      </v-avatar>
      <!-- <v-toolbar-title class="white--text font-weight-medium display-2">Software Campus</v-toolbar-title> -->
      <v-toolbar-title class="font-weight-medium display-1">Software Campus</v-toolbar-title>

      <template v-slot:extension>
        <!-- <v-toolbar-title class="white--text">Software Campus</v-toolbar-title> -->
        <v-spacer></v-spacer>
        <v-toolbar-items class="hidden-sm-and-down">
          <v-btn flat to="/home">Home</v-btn>
          <v-btn flat to="/about">About</v-btn>
          <v-btn flat to="/">Community</v-btn>
          <v-btn flat to="/">Event</v-btn>
          <v-btn flat to="/">Source Store</v-btn>
          <v-btn flat to="/">Notice</v-btn>
          <v-btn flat to="/">My Page</v-btn>
        </v-toolbar-items>
      </template>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>search</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>apps</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>refresh</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>more_vert</v-icon>
      </v-btn>
    </v-toolbar>
</template>

<script>
export default {
  // name: 'toolbar'
};
</script>

<style>
</style>

