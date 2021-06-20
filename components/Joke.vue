<template>

<nuxt-link :to="'jokes/' + id" class="joke-link">
  <b-card :style="{margin:margin}">
  <div class="joke">
  <b-card-text class="card-text">{{ joke }}</b-card-text>
  </div>
  </b-card>

  </nuxt-link>

</template>

<script>
export default {
    name:'Joke',
    props:[ 'joke','id' ],
    data(){
        return {
            margin:"12px"
        }
    }
}
</script>

<style>
.joke{
    padding: 1rem;
    margin: 1rem 0;
}
.card-text{
    text-decoration: none;
    font-size: 15px;
    color: #000;
}

</style>