<script>
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import { pokemonTypes } from './assets/scss/data'
export default {
  name: 'Pokedex',
  data: () => ({
    pokemonTypes
  }),
  components: {
    AppMain, AppHeader
  },
  methods: {
    changeType() {
      console.log('change')
    }
  }
};
</script>

<template>
  <AppHeader :pokemonTypes="pokemonTypes" @type-select-change="changeType" />
  <AppMain />
</template>

<style lang="scss">
@use './assets/scss/style.scss';
</style>
