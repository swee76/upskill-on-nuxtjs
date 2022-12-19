<template>
  <div>
    <div class="container">
      <Hero />
      <LargeCardDisplay
        v-for="largeCard in largeCardInfo"
        :key="largeCard.id"
        :cardsSection="largeCard"
      />
      <SmallCardDisplay
        v-for="smallCard in smallCardInfo"
        :key="smallCard.id"
        :cardsSection="smallCard"
      />
    </div>
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from "@/assets/data.js";
export default {
  name: "IndexPage",
  data() {
    return {
      largeCardInfo: largeCardSections,
      smallCardInfo: smallCardSections,
    };
  },
};
</script>
