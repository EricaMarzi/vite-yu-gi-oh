<script>
import axios from 'axios';
import { store } from '../assets/scss/data/store.js'
const endpoint = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons'
export default {
    name: 'PokemonList',
    data: () => ({
        store
    }),
    created() {
        axios.get(endpoint).then(res => {
            this.store = res.data.docs
        })
    }
};
</script>

<template>
    <div class="row row-cols-6 gap-3">
        <div class="col rounded py-2" v-for="pokemon in store">
            <div class="card-top d-flex justify-content-between">
                <h6>{{ pokemon.name }}</h6>
                <p>#{{ pokemon.number }}</p>
            </div>
            <div class="card-bottom d-flex mb-2">
                <div class="card-left d-flex flex-column justify-content-end gap-2">
                    <div class="badge rounded-pill text-bg-secondary">{{ pokemon.type1 }}</div>
                    <div class="badge rounded-pill text-bg-secondary">{{ pokemon.type2 }}</div>
                </div>
                <div class="card-right">
                    <img class="img-fluid" :src="pokemon.imageUrl" alt="">
                </div>
            </div>
        </div>
    </div>
    <!-- <div v-for="pokemon in pokemons"></div> -->
</template>

<style lang="scss" scoped>
@use '../assets/scss/bgcard.scss' as *;
@use '../assets/scss/vars.scss' as *;

.row {
    display: flex;
    justify-content: center;
}

.col {
    background-color: white;
}

.card-left {
    width: 50%;
}

.badge {
    width: fit-content;
}


.card-right {
    width: 50%;
    height: auto;
}
</style>