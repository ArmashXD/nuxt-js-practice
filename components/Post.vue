<template>
  <b-card>
      <b-card-text>{{id}}) {{title}}</b-card-text>
  </b-card>
</template>

<script>
export default {
    name:'Post',
    props:['id','title'],
    data(){
        return{
            post:''
        }
    }
}
</script>

<style>

</style>