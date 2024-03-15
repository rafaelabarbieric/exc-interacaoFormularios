<script setup>

  import { computed, ref } from 'vue'

  const texto = ref('')

</script>

<template>

  <h1>Formulário 1</h1>
  <input type="text" v-model="texto" placeholder="Seu nome">
  <p>{{ texto }}</p>
  
</template>

<style scoped>

</style>
