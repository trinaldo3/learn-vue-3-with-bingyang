<template>
    <div style="background-color: aqua; padding: 10px; margin: 20px;">
        <h2>This is the Component1 component.</h2>
    </div>
</template>

<script setup>
import { onBeforeMount, onBeforeUnmount, onBeforeUpdate, onMounted, onUnmounted, onWatcherCleanup, ref, watch } from 'vue'

console.log('Component1 is setup')

onBeforeMount(() => {
  console.log('componenent1 is before mount.')
})

onMounted(() => {
  console.log('componenet1 is mounted')
})

onBeforeUpdate(() => {
  console.log('componnent1 is before update.')
})

onUpdate(() => {
  console.log('componnent1 is updated.')
})

onBeforeUnmount(() => {
  console.log('componnent1 is before unmount.')
})

onUnmounted(() => {
  console.log('componnent1 is unmointed.')
})

</script>
