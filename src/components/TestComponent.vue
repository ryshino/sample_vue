<script setup>
import { ref } from 'vue'
const name = ref('')
defineProps({
  text: String,
})
const dataTest = 'これはデータです！'
</script>

<template>
  <p>{{ text }}</p>
  <p>{{ dataTest }}</p>
  <label>
    <span>名前</span>
    <input type="text" v-model="name" />
  </label>
  <p>ここの値が変わるよ→{{ name }}</p>
</template>
