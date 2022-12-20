<template>
  <div class="container">
    <MyItem v-for="item in myRentals" :key="item.id" :item="item" />
  </div>
</template>

<script>
import { mapState } from "vuex";
export default {
  name: "MyItemsPage",
  layout: "no-nav",
  computed: {
    ...mapState(["myRentals"]),
  },
};
</script>

<style scoped></style>
