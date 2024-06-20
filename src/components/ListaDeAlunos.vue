<template>
  <div>
    <Header />
    <div class="content">
      <h1>Lista de Alunos</h1>
      <ul>
        <li v-for="aluno in alunos" :key="aluno.id">
          {{ aluno.nome }}
        </li>
      </ul>
    </div>
    <Footer />
  </div>
</template>

<script>

export default {
  name: 'ListaDeAlunos',
  components: {
   
  },
  data() {
    return {
      alunos: []
    }
  },
  created() {
    
    this.alunos = [
      { id: 1, nome: 'Aluno 1' },
      { id: 2, nome: 'Aluno 2' },
         ]
  }
}
</script>

<style scoped>
.content {
  padding: 20px;
  background-color: #d3ffce;
  border-radius: 8px;
  min-height: 80vh;
  margin-bottom: 50px; 
}

ul {
  list-style: none;
  padding: 0;
}

li {
  background-color: #a2d5c6;
  padding: 10px;
  margin-bottom: 10px;
  border-radius: 8px;
}
</style>
