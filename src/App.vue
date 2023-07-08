<script setup>
  import { reactive, ref } from 'vue'

  const counter = reactive({ count: 4 })
  const message = ref('I am Leon')
</script>

<template>
   <h1>{{ message }}</h1>
   <p>The count is {{ counter.count }}</p>
</template>

<style scoped>

</style>
