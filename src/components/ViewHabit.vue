<template>
  <v-container>
    <v-layout
      text-center
      wrap
    >
    <a href="">Hello there</a>
    <a href="link.href">{{ link.text }}</a>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    link: [
      {
        text: 'Make a Habit',
        href: ''
      }
    ]
  })
}
</script>
