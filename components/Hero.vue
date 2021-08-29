<template>
  <div class="hero container">
    <div class="text-container">
      <h1 class="header">Find your Fire Extinguiser</h1>
      <p class="snippet">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Iste iusto
        illum quidem asperiores, cum nisi aperiam eius ipsa sapiente odit!
      </p>
      <button class="button btn">Start Looking</button>
    </div>
    <div class="image-container">
      <img src="~assets/svg/fire-extinguisher.svg" alt="" class="image" />
    </div>
  </div>
</template>

<script>
import { computed } from "vue";
import { useStore } from "@nuxtjs/composition-api";
export default {
  setup() {},
};
</script>

<style lang="scss" scoped>
.hero {
  position: relative;
  display: flex;
  padding: 5rem 0;
  align-items: flex-start;
  justify-content: space-between;
  .text-container {
    width: 50%;
    margin-top: 4rem;
    .header {
      font-weight: 900;
      font-size: 42px;
    }
    .snippet {
      color: grey;
      font-size: 22px;
    }
    .button {
      padding: 8px 25px;
      border-radius: 25px;
      background-color: rgb(231, 81, 43);
      color: white;
      width: 200px;
      font-weight: 700;
      transition: 0.5s;
    }
    .button:hover {
      width: 225px;
    }
  }
}
.image-container {
  width: 50%;
}
.image {
  display: block;
  margin: auto;
  width: 275px;
  margin-top: 2rem;
}
.overlay {
  background: rgba(0, 0, 0, 0);
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
}

@media (max-width: 500px) {
  .hero {
    height: 40vh;
  }
}
</style>