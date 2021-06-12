<template>
  <div :style="{margin:margin}">
      <b-form @submit.prevent="onSubmit">
      <b-form-input type="text" v-model="title" placeholder="Add Title" />
        <br>
       <b-form-input type="text" v-model="content" placeholder="Add Content" />
        <br>
 
        <button type="submit" class="btn btn-primary">Add </button>
        <br>
 
      </b-form>
  </div>
</template>

<script>
export default {
    name:'AddPost',
    data(){
        return{
            title:'',
            content:'',
            margin:"20px"
        }
    },
    methods:
    {
        onSubmit()
        {
            this.$emit('add-post', this.title, this.content)
            this.text='';

        }
    }
}
</script>

<style>

</style>