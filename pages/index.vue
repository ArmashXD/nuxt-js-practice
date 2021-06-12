<template>
  <div class="container">
    <h2>{{title}} </h2>
    
  </div>
</template>

<script>
export default {
  data(){
    return {
      title: 'Welcome to title'
    }
  },
  head(){
      return{
        title: "welcome to the site",
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
