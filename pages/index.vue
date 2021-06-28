<template>
  <div class="container">
    <h1>Nuxt App</h1>
    <Carousel />
    <br />
    <Card />
  </div>
</template>

<script>
import Carousel from "~/components/carousel.vue";
import Card from "~/components/card.vue";
export default {
  components: Carousel,
  Card,
};
</script>

<style>
.container {
  margin: 0 auto;
  display: flex;
  align-items: center;
  text-align: center;
  flex-direction: column;
  justify-content: space-between;
}
</style>
