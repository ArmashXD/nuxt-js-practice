<template>
  <b-form @submit.prevent="onSubmit" :style="{margin:margin}">
      <b-form-input type="text" v-model="text" placeholder="Search Jokes" />
    <input type="submit" value="Search Jokes"  /> 
  </b-form>
</template>

<script>
export default {
    name:'SearchJoke',
    data()
    {
        return {
            text: '',
            margin:"10px",
            
        }
    },
    methods:{
        onSubmit(){
            this.$emit('search-text', this.text);
            this.text='';
        }
    }
}
</script>

<style>

</style>