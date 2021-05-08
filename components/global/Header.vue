<template>
  <nav class="m-4" aria-label="Main Menu">
    <ul class="flex">
      <li class="flex-1 mr-auto">
        <nuxt-link class="btn block" to="/">RLW</nuxt-link>
      </li>
      <li class="flex-1 ml-2">
        <nuxt-link class="btn block" to="/blog">Blog</nuxt-link>
      </li>
      <li class="flex-1 ml-2">
        <nuxt-link class="btn block" to="/projects">Projects</nuxt-link>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'Header'
}
</script>
