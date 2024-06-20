<template>
  <div class="hello">
    <h1>{{ msg }}</h1> 
    <header class="header">
      <h1>Robótica Maria de Lurdes</h1>
    </header>

         <p>
      A robótica é uma área fascinante envolvendo engenharia, programação e inovação. 
      Nossas aulas de robótica  desperta a curiosidade e desenvolve habilidades essenciais. Desde a construção de modelos simples até
       programações de robôs avançados, nossos alunos aprendem de forma prática e divertida, aplicando conceitos de ciência, tecnologia, 
      engenharia e matemática (STEM). 
          </p>
        <ul>
      <li><a href="Link1" target="_blank" rel="noopener">Telefone 1</a></li> 
      <li><a href="Link2" target="_blank" rel="noopener">Telefone 2</a></li>
    </ul>
     
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
