<template>
    <div>
      <h3>{{ hData[index] }}</h3>
      <p>
        {{ textData[index] }}
      </p>
    </div>
  </template>
  
  <script setup lang="ts">
  
  const props = defineProps<{
    hData: string[],
    textData: string[],
    index: number
  }>()
  
  </script>
  
  <style scoped></style>
  