<script>
import axios from 'axios';
const endpoint = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons'
export default {
    name: 'PokemonList',
    data: () => ({
        pokemons: []
    }),
    created() {
        axios.get(endpoint).then(res => {
            this.pokemons = res.data.docs
        })
    }
};
</script>

<template>
    <div class="row row-cols-6 gap-3">
        <div class="col rounded">
            <div class="card-top d-flex justify-content-between">
                <h5>Bulbacoso</h5>
                <p>#001</p>
            </div>
            <div class="card-bottom d-flex mb-2">
                <div class="card-left d-flex flex-column justify-content-end gap-2">
                    <div class="badge rounded-pill text-bg-primary">Tipo 1</div>
                    <div class="badge rounded-pill text-bg-primary">Tipo 2</div>
                </div>
                <div class="card-right">
                    <img class="img-fluid" src="https://assets.pokemon.com/assets/cms2/img/pokedex/full/001.png" alt="">
                </div>
            </div>
        </div>
    </div>
    <!-- <div v-for="pokemon in pokemons"></div> -->
</template>

<style lang="scss" scoped>
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