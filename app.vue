<template>
  <div>
    <nav class="navbar container" role="navigation">
      <div class="navbar-brand">
        <nuxt-link to="/" class="navbar-item">
          Todo App
        </nuxt-link>
      </div>
      <div class="navbar-menu">
        <div class="navbar-end">
          <nuxt-link to="/" class="navbar-item">
            Home
          </nuxt-link>
          <nuxt-link to="/todo" class="navbar-item">
            Todo
          </nuxt-link>
        </div>
      </div>
    </nav>
    <NuxtPage />
  </div>
</template>

<script>
import 'bulma';

export default {
  render: {
    injectScripts: false,
  }
}
</script>
