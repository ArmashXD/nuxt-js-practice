<template>
  <div class="container">
      <h2>All Posts</h2>
      <AddPost v-on:add-post="addPost"/>
      <Post v-for="post in posts" :key="post.id" :id="post.id" :title="post.title"/>
  </div>
</template>

<script>
import axios from "axios";
import Post from "../../components/Post.vue";
import AddPost from '../../components/AddPost.vue';

export default {
  components:{
    Post, AddPost
  },
  data(){
    return {
      posts:[],
      csrf_token:this.$csrfToken()
    }
  },
  async created(){
    try {
       const config = {
            headers:{
                'Accept':'application/json',
            }
        }
        const res = await axios.get('http://localhost:8000/api/posts', config)
        this.posts = res.data;
    } catch (error) {
      console.log(error);
    }
  },
  methods:{
   async addPost(title, content)
    { 
      try {
          const res = await axios.post('http://localhost:8000/api/posts', { title: title, content:content }, {
      headers: {
        'content-type': 'text/json',
        'accept': '*/*',
      }
      });
      console.log(res)
      } catch (error) {
        
      console.log(error)
      }
    
    }
  }
}
</script>

<style>

</style>