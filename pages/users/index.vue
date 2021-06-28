<template>
  <div class="container">
    <b-col>
      <h1>{{ pageTitle }}</h1>
      <ul id="users">
        <li v-for="user in users" :key="user.name">
          <a href="#" @click.prevent="openUser(user)">{{ user.name }}</a>
        </li>
      </ul>
    </b-col>
  </div>
</template>

<script>
export default {
  async asyncData({ $axios }) {
    const users = await $axios.$get(
      `https://jsonplaceholder.typicode.com/users/`
    );
    return { users };
  },
  data: () => ({
    pageTitle: "Users page",
  }),

  methods: {
    openUser(user) {
      this.$router.push("/users/" + user.id);
    },
  },
};
</script>
<style scoped>
ul {
  display: flex;
  align-items: flex-start;
  justify-content: center;
  flex-direction: column;
}
</style>