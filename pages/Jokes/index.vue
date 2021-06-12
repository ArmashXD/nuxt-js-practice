<template>
    <div class="container">
        <SearchJokes v-on:search-text="searchText"/>
        <h1>Jokes</h1>
        <Joke v-for="joke in jokes" :key="joke.id" :id="joke.id" :joke="joke.joke"/>
    </div>
</template>
<script>
import axios from "axios";
import Joke from '../../components/Joke';
import SearchJokes from '../../components/SearchJokes.vue';

export default {
    components:{
        Joke,
        SearchJokes
    },
    data(){
        return {
            jokes: []
        }
    },
   async created(){
        const config = {
            headers:{
                'Accept':'application/json',
            }
        }
        try {
         const res = await axios.get('https://icanhazdadjoke.com/search', config);   
         this.jokes = res.data.results    
        } catch (error) {
            console.log(error)
        }
    },
    methods:{
       async searchText(text)
        {
             const config = {
            headers:{
                'Accept':'application/json',
            }
        }
        try {
         const res = await axios.get(`https://icanhazdadjoke.com/search?term=${text}`, config);   
         this.jokes = res.data.results    
        } catch (error) {
            console.log(error)
        }
        }
    },
     head(){
      return{
        title: "jokes",
        meta:[
          {
            hid:'index',
            name:'index',
            content:'best '
          }
        ]
      }
  }
}
</script>