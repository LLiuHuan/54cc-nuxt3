<script lang="ts" setup>
const route = useRoute()
const type = route.params.type

const data = await useAsyncData('one', () => $fetch('/api/one'))
console.log(data) // hello nuxt
</script>

<template>
  <div>
    {{ type }}
    {{ data }}
  </div>
</template>
