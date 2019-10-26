<template>
  <v-app>
    <v-content>
      <h1>Hi!</h1>
      <ViewHabit/>
    </v-content>
  </v-app>
</template>

<script>
import ViewHabit from './components/ViewHabit';
export default {
  name: 'App',
  components: {
    ViewHabit
  },
  data: () => ({
    //
  }),
};
</script>
