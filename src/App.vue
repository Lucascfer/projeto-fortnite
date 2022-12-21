<script>
import Banners from "./components/banners.vue";
import cardsVue from "./components/cards.vue";

export default {
  data() {
    return {
      heroData: null,
      bannerOpen: false
    };
  },

  components: {
    Banners,
    cardsVue,
  },

  methods: {
    onOpen(heroInfo) {
      this.bannerOpen = true
      this.heroData = heroInfo
    },

    onClose() {
      this.bannerOpen = false
      this.heroData = []
    },
  },
};
</script>

<template>
  <header>
    <h1>Projeto Fortnite</h1>
  </header>
  <div id="conteudo">
    <section>
      <h2>Selecione um personagem</h2>
      <Banners v-show="bannerOpen" :heroData="heroData" @close="onClose" />
      <cardsVue @open="onOpen" />
    </section>
  </div>
  <footer>
    <p>Criado por Lucascfer</p>
    <p class="links">
      <a href="https://github.com/Lucascfer" target="_blank">Github</a> |
      <a href="https://www.linkedin.com/in/lucas-carvalho-fernandes-799b9617a/" target="_blank">Linkedin</a>
    </p>
  </footer>
</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "FonteFortnite", sans-serif;
  list-style: none;
  text-decoration: none;
  justify-content: center;
  text-align: center;
  letter-spacing: 1px;
}

*::-webkit-scrollbar {
  width: 10px;
}

*::-webkit-scrollbar-track {
  background: #070d1200;
}

*::-webkit-scrollbar-thumb {
  background-color: aquamarine;
  border-radius: 25px;
  border: 2px solid rgb(58, 58, 58);
}

@font-face {
  font-family: "FonteFortnite";
  src: url("../public/fonte/Burbank\ Big\ Condensed\ Black.ttf");
}

header h1 {
  padding: 2rem 0 0 0;
  font-size: 4rem;
}

p,
h1,
h2:hover {
  cursor: default;
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
