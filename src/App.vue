<script>
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
export default {
  name: 'Pokedex',
  components: {
    AppMain, AppHeader
  }
};
</script>

<template>
  <AppHeader />
  <AppMain />
</template>

<style lang="scss">
@use './assets/scss/style.scss';
// @use './assets/scss/_vars.scss' as *;

// body {
//   background-color: $bg-color;
// }
</style>
