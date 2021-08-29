<template>
  <div>
    <div class="container">
      <Hero />
      <LargeCardDisplay
        v-for="(cardInfo, index) in largeCardInfo"
        :key="index"
        :cardsSection="cardInfo"
      />
      <SmallCardDisplay
        v-for="(cardInfo, index) in smallCardInfo"
        :key="index + 'a'"
        :cardsSection="cardInfo"
      />
    </div>
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from "@/assets/data.js";
export default {
  setup() {
    const largeCardInfo = largeCardSections;
    const smallCardInfo = smallCardSections;
    return { largeCardInfo, smallCardInfo };
  },
};
</script>

<style lang="scss" scoped>
</style>