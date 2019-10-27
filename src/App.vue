<template>
  <v-app>
    <v-app-bar
      absolute
      color="#43a047"
      dark
      shrink-on-scroll
      prominent
      src="https://picsum.photos/1920/1080?random"
      fade-img-on-scroll
      scroll-target="#scrolling-techniques-5"
      scroll-threshold="900">
      <template v-slot:img="{ props }">
        <v-img
          v-bind="props"
          gradient="to top right, rgba(55,236,186,.7), rgba(25,32,72,.7)">
        </v-img>
      </template>
      <v-toolbar-title class="headline text-uppercase">
        <span>Make a Habit</span>
        <span class="font-weight-light"></span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn
        text
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank">
        <span class="mr-2">SDHacks2019</span>
      </v-btn>
    </v-app-bar>
    <v-sheet
      id="scrolling-techniques-2"
      class="overflow-y-auto"
      max-height="600">
      <v-container style="height: 150px;"></v-container>
    </v-sheet>
    <v-content>
      <Homepage/>
    </v-content>
  </v-app>
</template>

<script>
import Homepage from './components/Homepage';

export default {
  name: 'App',
  components: {
    Homepage,
  },
};
</script>
