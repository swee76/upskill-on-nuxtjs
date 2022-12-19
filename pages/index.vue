<template>
  <div class="container">
    <Hero />
    <LargeCardDisplay
      v-for="largeCard in largeCardInfo"
      :key="largeCard.id"
      :cardsSection="largeCard"
    />
  </div>
</template>

<script>
import { largeCardSections } from "@/assets/data.js";
export default {
  name: "IndexPage",
  data() {
    return {
      largeCardInfo: largeCardSections,
    };
  },
};
</script>
