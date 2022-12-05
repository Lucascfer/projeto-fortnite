<script setup>
import cardsVue from './components/cards.vue';
</script>

<template>
  <header>
    <h1>Projeto Fortnite</h1>
  </header>
  <div id="conteudo">
    <section>
      <h2>Selecione um personagem</h2>
      <cardsVue />
    </section>
  </div>
  <footer>
    <p>Criado por Lucascfer</p>
    <p class="links"><a href="https://github.com/Lucascfer" target="_blank">Github</a> | <a
        href="https://www.linkedin.com/in/lucas-carvalho-fernandes-799b9617a/" target="_blank">Linkedin</a></p>
  </footer>
</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'FonteFortnite', sans-serif;
  list-style: none;
  text-decoration: none;
  justify-content: center;
  text-align: center;
  letter-spacing: 1px;
}

@font-face {
  font-family: 'FonteFortnite';
  src: url("../public/fonte/Burbank\ Big\ Condensed\ Black.ttf");
}

header h1 {
  padding: 2rem 0 0 0;
  font-size: 4rem;
}

section {
  padding: 0 1rem;
}

section h2 {
  padding: 1rem;
}

footer {
  font-size: 1.75rem;
  text-align: center;
  font-style: italic;
  color: aquamarine;
  bottom: 0px;
  padding-top: 2rem;
  padding-bottom: 1rem;
}

a {
  font-style: normal;
  font-size: 20px;
  color: aquamarine;
}

a:hover {
  cursor: pointer;
  color: rgb(2, 2, 132);
}
</style>