<template>
  <div>
    <h3>Customer Reviews</h3>
    <div v-if="reviews.results">
      <ReviewCard
        v-for="reviewer in reviews.results"
        :key="reviewer.login.uuid"
        :review="reviewer"
      />
    </div>
  </div>
</template>

<script>
import { ssrRef, useFetch } from "@nuxtjs/composition-api";

export default {
  setup() {
    const reviews = ssrRef(null);

    useFetch(async () => {
      reviews.value = await fetch("https://randomuser.me/api/?results=5").then(
        (res) => res.json()
      );
    });

    return { reviews };
  },
};
</script>

<style lang="scss" scoped>
</style>