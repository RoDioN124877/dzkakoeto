<template>
  <div>
    <section>
      <button @click="prevSlide">left</button>
      <div>
        <SliderC :hData="hData" :textData="textData" :index="index" />
      </div>
      <button @click="nextSlide">right</button>
    </section>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import SliderC from './sliderC.vue'

const hData = ref(['aaaaaa', 'bbbbb', 'ssssss'])
const textData = ref(['aaaaaa', 'bbbbb', 'ssssss'])
let index = ref(0)

const nextSlide = () => {
  index.value = (index.value + 1) % hData.value.length
}

const prevSlide = () => {
  index.value = (index.value - 1 + hData.value.length) % hData.value.length
}
</script>

<style scoped>
section {
  display: flex;
}
</style>
