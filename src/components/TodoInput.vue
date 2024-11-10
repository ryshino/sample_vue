<script setup lang="ts">
import { ref } from 'vue'

const input = ref('')
const inputDate = ref('')

function onSubmitForm() {
  console.log(input.value)
}
</script>

<template>
  <div>
    <form>
      <label>やること<input type="text" v-model="input" /></label>
      <label>期限<input type="date" v-model="inputDate" /></label>
      <input type="submit" @click="onSubmitForm" value="登録！" />
    </form>
  </div>
</template>
