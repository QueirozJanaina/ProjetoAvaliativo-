<template>
  <img alt="Vue logo" src="./assets/pronta.png">
  <HelloWorld />
   <div id="app">
   <ListaDeAlunos />
   <AulasDeMicrobit />
   <AulasDeRobóticas />
   <AulasDeScratch />
   <AulasDeSpikePrime /> 
  
  </div>
  </template>

<script>
import AulasDeMicrobit from './components/AulasDeMicrobit.vue';
import AulasDeRobóticas from './components/AulasDeRobóticas.vue';
import AulasDeScratch from './components/AulasDeScratch.vue';
import AulasDeSpikePrime from './components/AulasDeSpikePrime.vue';
import ListaDeAlunos from './components/ListaDeAlunos.vue';
import HelloWorld from './components/HelloWorld.vue';





export default {
 name: 'App',
 components: {
   ListaDeAlunos, HelloWorld, AulasDeMicrobit, AulasDeRobóticas, AulasDeScratch, AulasDeSpikePrime,
 }
};
</script>

<style>
/* Estilos globais */
#app {
 font-family: 'Avenir', Helvetica, Arial, sans-serif;
 text-align: center;
 color: #2c3e50;
 margin-top: 60px;
}
</style>