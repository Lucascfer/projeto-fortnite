<script setup>
const characters = [
    {
        id: 1,
        name: "Adira",
        icon: "/imagens/adira-icon.png",
        background: "/imagens/adira-tela.png",
        text: "lorem"
    },
    {
        id: 2,
        name: "Atemporal",
        icon: "/imagens/atemporal-icon.png",
        background: "/imagens/atemporal-tela.png",
        text: "lorem"
    },
    {
        id: 3,
        name: "Fedra",
        icon: "/imagens/fedra-icon.png",
        background: "/imagens/fedra-tela.png",
        text: "lorem"
    },
    {
        id: 4,
        name: "Imaginária",
        icon: "/imagens/imaginaria-icon.png",
        background: "/imagens/imaginaria-tela.png",
        text: "lorem"
    },
    {
        id: 5,
        name: "Malik",
        icon: "/imagens/malik-icon.png",
        background: "/imagens/malik-tela.png",
        text: "lorem"
    },
    {
        id: 6,
        name: "Midas",
        icon: "/imagens/midas-icon.png",
        background: "/imagens/midas-tela.png",
        text: "lorem"
    },
    {
        id: 7,
        name: "Ordem",
        icon: "/imagens/ordem-icon.png",
        background: "/imagens/ordem-tela.png",
        text: "lorem"
    },
    {
        id: 8,
        name: "Origem",
        icon: "/imagens/origem-icon.png",
        background: "/imagens/origem-tela.png",
        text: "lorem"
    },
    {
        id: 9,
        name: "Raz",
        icon: "/imagens/raz-icon.png",
        background: "/imagens/raz-tela.png",
        text: "lorem"
    }

]
</script>

<template>
    <div id="bannerList">
        <ul>
            <li v-for="hero in characters" :key="hero.id" class="hidden">
                <span>X</span>
                <div class="content">
                    <img :src=hero.icon :alt=hero.name class="icon">
                    <h2> {{ hero.name }} </h2>
                    <h3 class="text"> {{ hero.text }} </h3>
                </div>
                <img :src=hero.background class="background">
            </li>
        </ul>
    </div>
</template>

<style scoped>
.hidden {
    display: none;
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
}

#bannerList {
    position: absolute;
    padding: 5rem 20rem;
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
    padding: 0;
    display: flex;
    position: absolute;
    font-size: 55px;
    margin-top: 0.9rem;
}

.background {
    position: absolute;
    z-index: 7;
    border-radius: 15px;
    box-shadow: 0px 0px 600px 600px rgba(0, 0, 0, 0.632);
}

.text {
    display: block;
    z-index: 8;
    width: 28rem;
    font-size: 1rem;
    margin: auto;
    background-color: rgba(196, 196, 196, 0.737);
    padding: 3rem;
    border-radius: 15px;
}
</style>