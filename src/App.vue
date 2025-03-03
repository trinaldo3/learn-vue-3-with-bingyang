<template>
  <h1>{{ message }}</h1>
  <div class="card">
    <h2 ref="title">This is the App componenet.</h2>
    <h2>Number: {{ number }}</h2>
    <button @click="number++">Increment Number by one</button>
    <button @click="isShow = !isShow">Toggle component1</button>
    <Component1 v-if="isShow"></Component1>
  </div>
</template>

<script setup>
import { onBeforeMount, onBeforeUnmount, onBeforeUpdate, onMounted, onUnmounted, onWatcherCleanup, ref, watch } from 'vue'

import Component1 from './Component1.vue'

let message = ref('Hello, from Lifecycel Hooks!')

let number = ref(1)
let title = ref(null)

let isShow = true

console.log('App component is setup')

onBeforeMount(() => {
  console.log('App componenent is before mount.')
  console.log(number.value)
  console.log(title.value)
})

onMounted(() => {
  console.log('App componenet is mounted')
  console.log(title.value)
})

onBeforeUpdate(() => {
  console.log('App componnent is before update.')
})

onUpdate(() => {
  console.log('App componnent is updated.')
})

onBeforeUnmount(() => {
  console.log('App componnent is before unmount.')
})

onUnmounted(() => {
  console.log('App componnent is unmointed.')
})

watch(number, () => {
  console.log('Number changed!')
})
</script>

<style scoped>
.card {
  background-color: purple;
  color: white;
  padding: 20px 10px;
  margin-bottom: 10px;
}

</style>