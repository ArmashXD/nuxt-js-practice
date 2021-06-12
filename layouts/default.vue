<template>
  <div>
    <AppHeader/>
    <Nuxt />
  </div>
</template>

<script>
import AppHeader from '../components/AppHeader.vue';

export default {
  components:{
    AppHeader
  }
}
</script>

<style>
.joke-link{
    text-decoration: none;
}
</style>
