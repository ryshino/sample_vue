<script setup>
import { ref } from 'vue'
defineProps({
  text: String,
})
const name = ref('')
const dataTest = 'これはデータです！'
const fruitsList = ['りんご', 'いちご', 'バナナ']
</script>

<template>
  <p>{{ text }}</p>
  <p>{{ dataTest }}</p>
  <label>
    <span>名前</span>
    <input type="text" v-model="name" />
  </label>
  <p>ここの値が変わるよ→{{ name }}</p>
  <ul>
    <li v-for="fruit in fruitsList" :key="fruit">
      <p>{{ fruit }}</p>
    </li>
  </ul>
</template>
