<script>
import PokemonList from './PokemonList.vue'
export default {
    name: 'AppMain',
    components: { PokemonList }
};
</script>

<template>
    <main>
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

/*Pokedex*/
section#pokedex {
    background-color: #e6e6e6;
}
</style>
