<script setup>
import { ref } from "vue";

const valor2 = ref("");
const valor1 = ref("");
</script>
<template>
<div>
  

  <input type="number" v-model="valor1" placeholder="Total da conta" />

  <select name="Porcentagem da gorjeta" id="gorjeta" v-model="gorgeta">
    
    <option value="0">0%</option>
    <option value="5">5%</option>
    <option value="10">10%</option>
    <option value="15">15%</option>
    <option value="20">20%</option>
    <option value="25">25%</option>
    <option value="30">30%</option>
  </select>

  <input type="number" placeholder="Quantidade Dividida" v-model="valor2" />

  <p>Valor Individual: {{ (valor1 * (1 + gorgeta / 100)) / valor2 }}</p>
</div>
</template>
<style>
#gorjeta {
  background-color: aqua;
  margin: 5px;
  border-color: aliceblue;

}
body {
  background-color: rgb(241, 229, 229);

}
input{
  background-color: aqua;
  margin: 5px;
  border: 0px

}
div {
  
  background-color: rgb(198, 154, 240);
  display: flex;
  align-items: center;
  flex-direction: column;
  margin: 10% 30% 0 30% ;
}

</style>