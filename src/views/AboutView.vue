<template>
  <div class="about">
    <h1>This is an about page</h1>

    <div>count: {{ countStore.state.count }}</div>
    <button @click="count">add</button>
  </div>
</template>

<script setup lang="ts">
import { useCounterStore } from '@/stores/countStore'
const countStore = useCounterStore()
const count = () => countStore.add()
</script>

<style>
.about {
  border: 1px solid red;
  margin: 20px;
}
</style>
