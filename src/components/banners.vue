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
        <span class="iconX" @click="$emit('close')">X</span>
        <div class="content">
          <img :src="hero.icon" :alt="hero.name" class="icon" />
          <h2>{{ hero.name }}</h2>
          <h3 class="text">{{ hero.text }}</h3>
        </div>
        <img :src="hero.background" class="background" />
      </li>
    </ul>
  </div>
</template>

<style scoped>
.hidden {
  display: none;
  opacity: 0;
}

.heroList {
  position: relative;
  padding: 20rem 46.5rem;
  backdrop-filter: blur(10px);
  cursor: default;
  background-repeat: repeat;
}

span {
  z-index: 10;
  position: absolute;
  display: flex;
  font-size: 2rem;
  margin-top: 1rem;
  margin-left: 47rem;
}

span:hover {
  color: rgb(151, 2, 36);
  cursor: pointer;
}

.content {
  display: flex;
  position: absolute;
  width: 50rem;
  padding-top: 4rem;
  text-align: center;
  justify-content: center;
}

.content,
.background,
.iconX {
  display: flex;
  position: absolute;
  top: 6rem;
  left: 23rem;
}

#bannerList {
  position: absolute;
}

img {
  max-width: 50rem;
  justify-content: center;
  text-align: center;
  display: flex;
}

.icon {
  width: 15rem;
  z-index: 8;
  margin: 2rem auto;
  background-color: rgba(113, 113, 113, 0.737);
  padding: 0.5rem;
  border-radius: 25px;
}

h2 {
  z-index: 9;
  width: auto;
  height: auto;
  margin: 0;
  padding: 0 10px;
  display: flex;
  position: absolute;
  font-size: 55px;
  margin-top: 0.9rem;
  color: rgba(235, 232, 232, 0.737);
  background-color: #131313;
  border-radius: 15px;
  top: 7rem;
}

.background {
  z-index: 7;
  border-radius: 15px;
  /* box-shadow: 0px 0px 600px 600px rgba(0, 0, 0, 0.632); */
}

.text {
  font-family: "FonteFortnite", sans-serif;
  display: block;
  z-index: 8;
  width: 28rem;
  max-height: 200px;
  overflow-y: auto;
  font-size: 1.5rem;
  margin: auto;
  background-color: rgba(235, 232, 232, 0.737);
  color: #131313;
  padding: 3rem;
  border-radius: 15px;
}
</style>
