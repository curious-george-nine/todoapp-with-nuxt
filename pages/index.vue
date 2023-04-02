<template>
  <section class="hero is-fullheight-with-navbar">
    <div class="hero-body">
      <div class="container has-text-centered">
        <h1 class="title">Todo App</h1>
        <nuxt-link to="/todo" class="button is-primary is-large">
          Start managing todos
        </nuxt-link>
      </div>
    </div>
  </section>
</template>

<style>
  .nuxt-link {
    color: unset !important;
  }
</style>