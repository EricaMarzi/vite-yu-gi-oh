<script>
import PokemonList from './PokemonList.vue'
export default {
    name: 'AppMain',
    components: { PokemonList }
};
</script>

<template>
    <main>
        <!--lucine pokedex-->
        <section id="light" class="d-flex gap-2 align-items-end p-5">
            <div class="rounded-circle big blue"></div>
            <div class="rounded-circle small red"></div>
            <div class="rounded-circle small yellow"></div>
            <div class="rounded-circle small green"></div>
        </section>

        <section id="pokedex" class="container rounded">
            <div class="py-4">
                <PokemonList />
            </div>
        </section>
    </main>
</template>

<style lang="scss" scoped>
@use '../assets/scss/_vars.scss' as *;

main {
    height: 100vh;
    width: 100%;
    background-color: $bg-color;
}

/* Luci pokedex */
.big {
    height: 50px;
    width: 50px;
    border: 2px solid white;
}

.small {
    height: 25px;
    width: 25px;
    border: 2px solid white;
}

.blue {
    background-color: $circle-blue;
    // background-size: 50px 50px;
    // background-color: linear-gradient(to bottom right, white, $circle-blue);
}

.red {
    background-color: $circle-red;
}

.yellow {
    background-color: $circle-yellow;
}

.green {
    background-color: $circle-green;
}

/*Pokedex*/
section#pokedex {
    background-color: #e6e6e6;
    min-height: 400px;
}
</style>
