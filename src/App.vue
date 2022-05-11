<script setup>
import SlideControl from './components/SlideControl.vue';
</script>

<template>
  <SlideControl />
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 10px;
  justify-items: center;
}

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