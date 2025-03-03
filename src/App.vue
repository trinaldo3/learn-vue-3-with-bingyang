<template>
  <h1>{{ message }}</h1>
  <button @click="sortUsersByAge">Sort Users by age</button>
  <button @click="hideInactiveUSer">Hide Inactive Users</button>
  <button @click="showFirstTwoUsers">Show First Two User</button>
  <ul>
    <li v-for="(user, index) in users" :key="user.id">
      {{ index }} - {{ user.id }} - {{ user.name }} - {{ user.age }} - 
      {{ user.isActive }}
    </li>
  </ul>
</template>

<script setup>
import { ref } from 'vue'

let message = ref('Hello, Array Change Detection!')

const users = ref([
  { id: 1001, name: 'John Smith', age: 26, isActive: false },
  { id: 1002, name: 'Tom Doe', age: 16, isActive: false },
  { id: 1003, name: 'Franklin Wong', age: 18, isActive: true } 
])

function sortUsersByAge() {
  users.value.sort((a,b) => a.age - b.age)
}

function hideInactiveUSer() {
  users.value = users.value.filter((user) => user.isActive)
}

function showFirstTwoUsers() {
  users.value = users.value.slice(0,2)
}
</script>

<style scoped>

</style>