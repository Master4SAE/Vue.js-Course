<script setup>
import { ref } from 'vue';

const name = ref("Sohaib");
const href = ref("https://vuejs.org/")
const myButtonDisable = ref(false)
const codingYears = ref(3)
const portfolio = ref("https://my-portfolio-d54ab.web.app")
const blockLeave = () => {
  alert("You cant leave this page!");
};
</script>

<template>
  <h1>Hello my name is <a v-on:click=[blockLeave()] v-bind:href="portfolio" target="_blank">{{ name }}</a></h1>
  <p>
    Visit 
    <a v-bind:href="href" target="_blank" rel="noopener">vuejs.org</a> to read the
    documentation
  </p>
  <p>
    {{
      (codingYears > 0 ? "I have been coding for " + codingYears + " years " : "I am a noob") 
    }} </p>
  <button v-on:click="codingYears++" v-bind:disabled="myButtonDisable"> Click me </button>
</template>

<style scoped></style>
