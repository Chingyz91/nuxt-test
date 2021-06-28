<template>
  <div>
    <b-navbar toggleable="lg" type="dark" variant="info">
      <b-navbar-brand href="#">NavBar</b-navbar-brand>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav class="nav-links">
          <nuxt-link class="nav-links" to="/">About</nuxt-link>
          <nuxt-link class="nav-links" to="/users">Users</nuxt-link>
          <nuxt-link class="nav-links" to="/login">login</nuxt-link>
          <nuxt-link class="nav-links" to="/posts">Posts</nuxt-link>
          <nuxt-link class="nav-links" to="/todos">Todos</nuxt-link>
          <nuxt-link class="nav-links" to="/comments">Comments</nuxt-link>
        </b-navbar-nav>

        <b-navbar-nav class="ml-auto">
          <b-nav-item-dropdown text="Lang" right>
            <b-dropdown-item href="#">EN</b-dropdown-item>
            <b-dropdown-item href="#">RU</b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<style>
.nav-links {
  text-decoration: none;
  color: black;
  margin-right: 10px;
}
</style>
