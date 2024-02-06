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
  }
};
</script>

<template>
  <AppHeader :pokemonType="pokemonType" />
  <AppMain />
</template>

<style lang="scss">
@use './assets/scss/style.scss';
// @use './assets/scss/_vars.scss' as *;

// body {
//   background-color: $bg-color;
// }
</style>
