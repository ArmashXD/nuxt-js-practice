<template>
<div>
   <b-navbar type="dark" variant="dark" >
    <b-navbar-nav class="ml-auto">
      <b-nav-item > <nuxt-link to="/" class="joke-link" style="color:white">Home</nuxt-link></b-nav-item>
    <b-nav-item > <nuxt-link to="/posts/all" class="joke-link" style="color:white">Posts</nuxt-link></b-nav-item>
       
      <b-nav-item > <nuxt-link to="/about" class="joke-link" style="color:white">About</nuxt-link></b-nav-item>


    </b-navbar-nav>
  </b-navbar>
            <!-- <li>
                <nuxt-link to='/'>Home</nuxt-link>
            </li>
            <li>
                <nuxt-link to='/jokes'>Jokes</nuxt-link>
            </li>
            <li>
                <nuxt-link to='/about'>About</nuxt-link>
            </li> -->
            <br><br>
  </div>

</template>

<script>
export default {
    name:'AppHeader'

}
</script>

<style>

</style>