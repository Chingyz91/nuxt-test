<template>
  <section>
    <div class="container">
      <h2>
        {{ pageTitle }}
      </h2>
      <h4 v-for="todo in todos" :key="todo.title">
        {{ todo.title }}
      </h4>
    </div>
  </section>
</template>

<script>
export default {
  async asyncData({ $axios }) {
    const todos = await $axios.$get(
      `https://jsonplaceholder.typicode.com/todos?_limit=10`
    );
    return { todos };
  },

  data: () => ({
    pageTitle: "Todos",
  }),
};
</script>

<style scoped>
h4 {
  border: solid 1px;
}
</style>