<template>
  <v-container>
    <v-layout
      text-center
      wrap
    >
      <a href="">{{ viewlink.text }}</a>
      <a :href="viewlink.href">{{ viewlink.text }}</a>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    viewlink: [
      {
        text: 'Make a Habit',
        href: ''
      }
    ]
  })
}
</script>
