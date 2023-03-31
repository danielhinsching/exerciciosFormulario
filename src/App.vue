<script setup>
import { ref } from 'vue'
const nome = ref('')
const texto = ref('')
const aceita = ref(false)
</script>

<template>
    <div class="info">
      <p>Nome:</p>
      <input type="text" v-model="nome"/>
      <p>idade:</p>
      <input type="number" v-model="idade" max="2"/>
      <p>email:</p>
      <input type="email" v-model="email"/>
      <p>.</p>
      <button>Enviar</button>
      <p>aceita os termos:</p>
      <label for="aceita">Aceito os termos</label>
      
    </div>
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
