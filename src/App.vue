<script setup>
import { ref } from 'vue'
const nome = ref('')
const email = ref('')
const senha = ref('')
const confirmaSenha = ref('')
const data = ref('')
const endereço = ref('')
const cidade = ref('')
const estado = ref('')
const hobbies = ref('')
const linguagemProg = ref('')
const biografia = ref('')

const aceitar = ref(false)

function enviar() {
  aceitar.value = !aceitar.value
  nome.value = ''
  idade.value = ''
  email.value = ''
}
</script>

<template>
    <form class="info" @submit.prevent="enviar()">
      <p>Nome:</p>
      <input type="text" v-model="nome" minlength="3" maxlength="20"/>
      <p>email:</p>
      <input type="email" v-model="email"/>
      <p>senha:</p>
      <input type="password" v-model="senha">
      <p>confirmar senha:</p>
      <input type="password" v-model="confirmaSenha">
      <p>data de nascimento:</p>
      <input type="date" v-model="data">
      <p>endereço:</p>
      <input type="text" v-model="endereço">
      <P>cidade:</P>
      <input type="string" v-model="cidade">
      <p>estado:</p>
      <input type="string" v-model="estado">
      <p>hobbies:</p>
      <input type="text" v-model="hobbies">
      <p>linguagem de Programação:</p>
      <p>biografia:</p>





      <hr>
      <button type="submit">Enviar</button>
      <div v-if="aceitar">
        <p>{{ nome }}</p> 
        <p>{{ idade }}</p>
        <p>{{ email }}</p>
      
      </div>
    </form>
  
</template>


<style scoped>
.info {
  background-color: rgba(35,12,22,1);
  padding: 20px 30px;
  color: rgb(183, 210, 219);
  border-radius: 10px;
}

h1 {
  color: white;
  font-weight: bold;
  font-size: 1.5em;
}
</style>
