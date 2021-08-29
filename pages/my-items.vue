<template>
  <div class="container">
    <MyItem v-for="rental in myRentals" :key="rental.id" :item="rental" />
  </div>
</template>

<script>
import { useStore } from "@nuxtjs/composition-api";
export default {
  layout: "no-nav",
  setup() {
    const store = useStore();
    const myRentals = store.state.myRentals;
    return { myRentals };
  },
};
</script>

<style lang="scss" scoped>
</style>