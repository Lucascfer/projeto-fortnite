<script>
export default {
    name: "cards",
    data() {
        return {
            characters: [],
        };
    },
    methods: {
        async getData() {
            const req = await fetch("cards.json");
            const data = await req.json()
            this.characters = data.Character
        },

    },
    mounted() {
        this.getData();
    },
}
</script>

<template>
    <div>
        <ul>
            <li v-for="hero in characters" :key="hero.id" :id="hero.id">
                <img :src=hero.icon :alt=hero.name>
                <p class="heroName" @click="$emit('open', hero)"> {{ hero.name }}</p>
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