<script setup>

  import { ref } from 'vue'

  let nome = ref ('')
  let idade = ref ('')
  let email = ref ('')

  const dados = ref(true)


  let nome2 = ref ('')
  let idade2 = ref ('')
  let email2 = ref ('')

  const dados2 = ref(true)

</script>

<template>

  <div>
    <section v-if="dados">
      <h1>Formulário 1</h1>
      <form>
        <label for="name">Seu Nome:</label>
        <input type="text" id="name" v-model="nome">

        <label for="idade">Sua Idade:</label>
        <input type="number" id="idade" v-model="idade">

        <label for="e-mail">Seu Email:</label>
        <input type="email" id="e-mail" v-model="email">
      </form>
      <button  @click="dados = false">Enviar</button>
    </section>
    <section v-else>
      <h1>Seus dados:</h1>
      <p>Nome: {{ nome }}</p>
      <p>Idade: {{ idade }}</p>
      <p>E-mail: {{ email }}</p>
      <button  @click="dados = true">Voltar</button>
    </section>
  </div>

  <div>
    <section v-if="dados2">
      <h1>Formulário 2</h1>
      <form>
        <label id="li" for="name">Seu Nome:</label>
        <input type="text" id="name" v-model="nome2" maxlength="20"  minlength="3">

        <label for="idade">Sua Idade:</label>
        <input type="number" id="idade" v-model="idade2" max="60"  min="18">

        <label for="e-mail">Seu Email:</label>
        <input type="email" id="e-mail" v-model="email2">
      </form>
      <button  @click="dados2 = false">Enviar</button>
    </section>
    <section v-else>
      <h1>Seus dados:</h1>
      <p>Nome: {{ nome2 }}</p>
      <p>Idade: {{ idade2 }}</p>
      <p>E-mail: {{ email2 }}</p>
      <button  @click="dados2 = true">Voltar</button>
    </section>
  </div>
  
</template>

<style scoped>

div {
  width:25%;
}

</style>
