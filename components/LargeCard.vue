<template>
  <NuxtLink :to="`/products/${card.id}`" class="card">
    <img
      :src="require(`@/assets/images/${card.image || 'fe1.jpg'}`)"
      alt=""
      class="image"
    />
    <h3 class="header">{{ card.title }}</h3>
    <p class="snippet">{{ card.snippet }}</p>
  </NuxtLink>
</template>

<script>
export default {
  props: ["card"],
};
</script>

<style lang="scss" scoped>
.card {
  width: 31.5%;
  height: 25rem;
  border: none;
  overflow: hidden;
  padding: 0;
  cursor: pointer;
  a {
    &:hover {
      text-decoration: none;
    }
  }
}
.image {
  height: 65%;
  border-radius: 0.5rem;
}
.header {
  font-size: 1.15rem;
  margin-top: 0.4rem;
  color: #000;
  &:hover {
    text-decoration: none;
    color: #000;
  }
}
.snippet {
  color: grey;
}
</style>