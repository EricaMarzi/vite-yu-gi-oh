<script>
export default {
    name: 'PokemonType',
    props: {
        pokemonType: Array
    },
    emits: ['type-select-change']
}
</script>

<template>
    <header class="p-5 d-flex justify-content-between align-items-center">
        <section id="light" class="d-flex gap-2 align-items-start">
            <div class="rounded-circle big blue"></div>
            <div class="rounded-circle small red"></div>
            <div class="rounded-circle small yellow"></div>
            <div class="rounded-circle small green"></div>
        </section>

        <section id="select-type">
            <select class="form-select" @change="$emit('type-select-change')">
                <option selected>All</option>
                <option v-for="(type, i) in pokemonType" :key="i" :value="i"> {{ type }}</option>
            </select>
        </section>
    </header>
</template>

<style lang="scss" scoped>
@use '../assets/scss/_vars.scss' as *;

header {
    background-color: $bg-color;
}

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
</style>