<template>
  <div>
    <Nav />
    <div class="container">
      <LargeCardDisplay
        v-for="largeCard in largeCardInfo.slice(0, 1)"
        :key="largeCard.id"
        :cardsSection="largeCard"
      />
      <SmallCardDisplay
        v-for="smallCard in smallCardInfo.slice(0, 1)"
        :key="smallCard.id"
        :cardsSection="smallCard"
      />
    </div>
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from "@/assets/data.js";
export default {
  name: "ProductPage",
  data() {
    return {
      largeCardInfo: largeCardSections,
      smallCardInfo: smallCardSections,
    };
  },
};
</script>

<style></style>
