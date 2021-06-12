<template>
  <div class="container">
     <Hero/>
     <LargeCardDisplay
     v-for="cardInfo in largeCardInfo"
     :key="cardInfo.id"
     :cardsSection="cardInfo"
     />
    <SmallCardDisplay
    v-for="cardInfo in smallCardInfo"
    :key="`${cardInfo.title }`"
    :cardsData="cardInfo"
    />
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from "@/assets/data.js"

export default {

  data(){
    return {
      largeCardInfo: largeCardSections,
      smallCardInfo: smallCardSections
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
