<script>
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import { pokemonType } from './assets/scss/data'
export default {
  name: 'Pokedex',
  data: () => ({
    pokemonType
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
  <AppHeader :pokemonType="pokemonType" @type-select-change="changeType" />
  <AppMain />
</template>

<style lang="scss">
@use './assets/scss/style.scss';
</style>
