<template>
  <div>
    <Header />
    <div class="content">
      <h1>Aulas de Scratch</h1>
      <form @submit.prevent="inscreverAluno">
        <div>
          <label>Nome do Aluno:</label>
          <input type="text" v-model="novoAluno.nome" required>
        </div>
        <button type="submit">Inscrever-se</button>
      </form>

      <h2>Projetos Postados</h2>
      <form @submit.prevent="postarProjeto">
        <div>
          <label>Nome do Projeto:</label>
          <input type="text" v-model="novoProjeto.nome" required>
        </div>
        <div>
          <label>Descrição do Projeto:</label>
          <textarea v-model="novoProjeto.descricao" required></textarea>
        </div>
        <button type="submit">Postar Projeto</button>
      </form>

      <ul>
        <li v-for="projeto in projetos" :key="projeto.id">
          <h3>{{ projeto.nome }}</h3>
          <p>{{ projeto.descricao }}</p>
          <p>Nota: {{ projeto.nota }}</p>
          <p>Comentários: {{ projeto.comentarios }}</p>
        </li>
      </ul>
    </div>
    <Footer />
  </div>
</template>

<script>


export default {
  name: 'AulasDeScratch',
  components: {
    
  },
  data() {
    return {
      novoAluno: { nome: '' },
      alunos: [],
      novoProjeto: { nome: '', descricao: '', nota: '', comentarios: '' },
      projetos: []
    }
  },
  methods: {
    inscreverAluno() {
      if (this.alunos.length < 30) {
        this.alunos.push({ ...this.novoAluno })
        this.novoAluno.nome = ''
      } else {
        alert('Limite de alunos atingido')
      }
    },
    postarProjeto() {
      this.projetos.push({ ...this.novoProjeto, id: Date.now() })
      this.novoProjeto.nome = ''
      this.novoProjeto.descricao = ''
      this.novoProjeto.nota = ''
      this.novoProjeto.comentarios = ''
    }
  }
}
</script>

<style scoped>
.content {
  padding: 20px;
  background-color: #f0f8ff;
  border-radius: 8px;
  min-height: 80vh;
  margin-bottom: 50px;
}

form {
  margin-bottom: 20px;
}

form div {
  margin-bottom: 10px;
}

button {
  background-color: #42b983;
  color: white;
  border: none;
  padding: 10px 20px;
  cursor: pointer;
}

button:hover {
  background-color: #2c3e50;
}

ul {
  list-style: none;
  padding: 0;
}

li {
  background-color: #e6e6fa;
  padding: 10px;
  margin-bottom: 10px;
  border-radius: 8px;
}
</style>
