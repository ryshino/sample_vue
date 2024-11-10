<script setup lang="ts">
import { ref } from 'vue'
defineProps({
  text: String,
})
const name = ref('')
const dataTest = 'これはデータです！'
const fruitsList = ['りんご', 'いちご', 'バナナ']
const number = 5
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
  <div>
    <p v-if="number < 10">数字は10より小さいです</p>
    <p v-else>数字は10より大きいです</p>
    <p v-show="number > 10">数字は10より小さいです(v-show)</p>
  </div>
</template>
