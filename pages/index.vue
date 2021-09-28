<template>
  <div>
    <div class="container">
      <Hero />
      <LargeCardDisplay
        v-for="cardInfo in largeCardInfo"
        :key="cardInfo.id"
        :cards-section="cardInfo"
      />

      <SmallCardDisplay
        v-for="cardInfo in smallCardSections"
        :key="cardInfo.id"
        :cards-section="cardInfo"
      />
    </div>
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from '@/assets/data.js'

export default {
  data () {
    return {
      largeCardInfo: largeCardSections,
      smallCardSections
    }
  }
}
</script>
