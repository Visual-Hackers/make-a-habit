<template>
  <v-app>
    <v-content>
      <List></List>
    </v-content>
  </v-app>
</template>

<script>
//import HelloWorld from "./components/HelloWorld";
import List from "./components/List";

export default {
  name: "App",
  components: {
    //HelloWorld
    List
  },
  data: () => ({
    //
  })
};
</script>
