<template>
  <section>
    <div class="container">
      <h2>
        {{ pageTitle }}
      </h2>
      <h4 v-for="post in posts" :key="post.title">
        {{ post.title }}
      </h4>
    </div>
  </section>
</template>

<script>
export default {
  async asyncData({ $axios }) {
    const posts = await $axios.$get(
      `https://jsonplaceholder.typicode.com/posts`
    );
    return { posts };
  },

  data: () => ({
    pageTitle: "Posts",
  }),
};
</script>

<style scoped>
h4 {
  border: solid 1px;
}
</style>