<template>
  <div>
    <SmallCardDisplay v-for="cards in smallCardSections" :key="cards.id" :cardsData="cards"/>
  </div>
</template>

<script>
import { smallCardSections } from "@/assets/data.js"

export default {
  head(){
    return {
      title:"Products"
    }
  },
  data(){
    return {
      smallCardSections:smallCardSections
    }
  }
  //  computed:{
  //       products(){
  //           return this.$store.getters.getAllProducts();
  //       }
  //   }
}
</script>

<style>

</style>