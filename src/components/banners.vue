<script>
export default {
  name: "cards",

  data() {
    return {
      hero: {},
      heroLi: null,
    };
  },

  props: {
    heroData: {},
  },

  updated() {
    this.hero = this.heroData;
  },
};
</script>

<template>
  <div id="bannerList">
    <ul>
      <li :key="hero.id" class="heroList" :id="hero.id">
        <div class="content" :style="{ backgroundImage: `url(${hero.background})` }">
          <span class="iconX" @click="$emit('close')">X</span>
          <img :src="hero.icon" :alt="hero.name" class="icon" />
          <h2 class="heroName">{{ hero.name }}</h2>
          <h3 class="text">{{ hero.text }}</h3>
        </div>
      </li>
    </ul>
  </div>
</template>

<style scoped>
.content {
  position: absolute;

  border-radius: 15px;
  margin: 5rem auto;
  padding: 3rem;
  background-repeat: no-repeat;
  background-size: auto;
  background: 100%;
  background-position: center;

  display: grid;
  grid-template-columns: repeat(5, 1fr);
  grid-template-rows: repeat(5, 1fr);
  grid-column-gap: 0px;
  grid-row-gap: 0px;
}

.hidden {
  display: none;
  opacity: 0;
}

.heroList {
  display: flex;
  cursor: default;
}

.iconX {
  grid-area: 1 / 5 / 3 / 6;
  z-index: 10;
  font-size: 2rem;
  padding: 1px 10px;
  margin: 0 0 1rem auto;
  align-self: flex-start;
  align-content: flex-start;
  align-items: flex-start;
  background-color: aquamarine;
  border-radius: 15px;
}

.iconX:hover {
  background-color: rgb(151, 2, 36);
  color: aquamarine;
  cursor: pointer;
}

.icon {
  grid-area: 1 / 1 / 6 / 3;
  max-width: 50rem;
  justify-content: center;
  text-align: center;
  width: 15rem;
  z-index: 8;
  margin: auto;
  background-color: rgba(113, 113, 113, 0.737);
  padding: 0.5rem;
  border-radius: 25px;
}

.heroName {
  grid-area: 1 / 3 / 3 / 5;
  z-index: 9;
  font-size: 55px;
  color: rgba(235, 232, 232, 0.737);
  background-color: #131313;
  border-radius: 15px;
  padding: 0.5rem 0.5rem 0.5rem 0;
  margin: 1rem 2rem 1rem 0;
  align-self: flex-start;
  align-content: flex-start;
  align-items: flex-start;
}

.text {
  grid-area: 3 / 3 / 6 / 6;
  font-family: "FonteFortnite", sans-serif;
  z-index: 8;
  width: 28rem;
  max-height: 200px;
  overflow-y: auto;
  font-size: 1.5rem;
  margin: auto;
  background-color: rgba(235, 232, 232, 0.737);
  color: #131313;
  padding: 2rem 1rem;
  border-radius: 15px;
}

@media (max-width: 950px) {
  .content {
    padding: 5px;
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: repeat(5, 1fr);
    grid-column-gap: 0px;
    grid-row-gap: 0px;
  }

  .heroName {
    grid-area: 1 / 1 / 2 / 2;
    padding: 0.5rem 1rem;
    margin: 1rem 0;
    align-self: flex-end;
    align-content: flex-end;
    align-items: flex-end;
    font-size: 2rem;

  }

  .iconX {
    grid-area: 1 / 2 / 2 / 3;
    align-self: flex-start;
    align-content: flex-start;
    align-items: flex-start;
    margin: 2rem 0 2rem 5rem;
    padding: 0;
    background-color: transparent;
  }

  .icon {
    grid-area: 2 / 1 / 4 / 3;
  }

  .text {
    grid-area: 4 / 1 / 6 / 3;
    width: 20rem;
    font-size: 1.1rem;
    text-align:start;
  }
}
</style>
