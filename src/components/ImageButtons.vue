<script setup>
  const props = defineProps({
    title: String,
  })
</script>

<template>
  <button class="active">
    {{title}}
  </button>
</template>

<style scoped>

button {
  background-color: lightblue;
  border: none;
  color: white;
  padding: 15px 30px;
  margin: 10px;
  text-align: center;
  text-decoration: none;
  font-size: 2rem;
  border-radius: 10px;
  cursor: pointer;
  width: 50%;
}

h1 {
  color: lightblue;
  font-size: 3em;
}
</style>