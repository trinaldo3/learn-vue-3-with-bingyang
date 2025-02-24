<template>
  <h1>message: {{ message }}</h1>
  <hr>
  <h1>number: {{ number }}</h1>
  <hr>
  <h1>doubleNum(50): {{ doubleNum(50) }}</h1>
  <hr>
  <h1>number * 2 = {{ number * 2 }}</h1>
  <hr>
  <h1>{{ number > 150? 'number is greater than 150':'number is less than 150' }}</h1>
  <hr>
  <h1 v-text="number"></h1>
  <hr>
  <h1>{{ harry }}</h1>
  <hr>
  <h1>{{ harry.name }}</h1>
  <hr>
  <h1>{{ hogwartsWizards }}</h1>
  <h1>{{ hogwartsWizards[0] }}</h1>
  <hr>
  <h1>{{ rawHtml }}</h1>
  <h1 v-text="rawHtml"></h1>
  <h1 v-html="rawHtml"></h1>

</template>

<script setup>
let message = 'Hello, Vue!'
let number = 50

function doubleNum(num){
  return num * 2
}


let harry = {
  id: 1001,
  name: 'Harry Potter',
  house: 'Gryffindor',
  age: 17,
  wand: {
    core: 'phoenix feather',
    wood: 'holly',
  }
}


const hogwartsWizards = [
  {
    id: 1001,
    name: 'Harry Potter',
    house: 'Gryffindor',
    age: 17,
    wand: {
      core: 'phoenix feather',
      wood: 'holly',
    }
  },
  {
    id: 1002,
    name: 'Hermione Granger',
    house: 'Gryffindor',
    age: 17,
    wand: {
      core: 'dragon heartstring',
      wood: 'vine',
    }
  },
  {
    id: 1003,
    name: 'Ron Weasley',
    house: 'Gryffindor',
    age: 17,
    wand: {
      core: 'unicorn hair',
      wood: 'willow',
    }
  },
  {
    id: 1004,
    name: 'Draco Malfoy',
    house: 'Slytherin',
    age: 17,
    wand: {
      core: 'dragon heartstring',
      wood: 'hawthorn',
    }
  }
]

let rawHtml = '<span style="color: red">This should be red</span>'
</script>

<style lang="scss" scoped></style>