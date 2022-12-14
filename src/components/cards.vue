<script>
export default {
    // name: "cards",
    // data() {
    //     return {
    //         characters: [],
    //     };
    // },
    // methods: {
    //     async getData() {
    //         const req = await fetch("cards.json");
    //         const data = await req.json()
    //         this.characters = data.Character
    //     },
    // },
    // mounted() {
    //     this.getData();
    // },
    setup() {
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

        ];

        return {
            characters,

        }
    },
}
</script>

<template>
    <div>
        <ul>
            <li v-for="hero in characters" :key="hero.id" class="umaclasse" :id="hero.id">
                <img :src=hero.icon :alt=hero.name>
                <p class="heroName"> {{ hero.name }}</p>
            </li>
        </ul>
    </div>
</template>

<style scoped>
div {
    background-color: aquamarine;
    border-radius: 7px;
    min-width: auto;
}

ul {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: space-evenly;
    padding: 1.5rem;
}

img {
    margin: 5px;
    padding: 5px;
    background-color: rgba(113, 113, 113, 0.253);
    border-radius: 35px;
    height: 250px;
    width: 250px;
    box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
}

p {
    color: aquamarine;
    background-color: rgb(95, 94, 94);
    text-align: center;
    position: relative;
    padding: 5px 20px;
    border-radius: 15px;
    margin: auto;
    width: min-content;
    box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.475);
    top: -50px;
    opacity: 0;
}

p:hover {
    background-color: aquamarine;
    color: rgb(95, 94, 94);
}

li:hover p {
    opacity: 1;
    transform: translateY(45px);
    transition: all .4s;
}

p:hover {
    cursor: pointer;
}
</style>