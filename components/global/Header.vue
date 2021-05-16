<template>
  <div class="flex flex-col md:flex-row items-center md:justify-between mb-4">
    <a class="p-4 dark:text-white font-cursive uppercase" href="/">Rebecca Louise Writes</a>
    <nav class="m-4" aria-label="Main Menu">
      <ul class="flex flex-wrap justify-center text-sm">
        <li class="ml-2 mb-5">
          <nuxt-link class="py-2 mx-2 dark:text-white border-b dark:border-white" to="/blog">Blog</nuxt-link>
        </li>
        <li class="ml-2 mb-5">
          <nuxt-link class="py-2 mx-2 dark:text-white border-b dark:border-white" to="/projects">Other work</nuxt-link>
        </li>
        <li v-for="(page, index) in pages" :key="index" class="ml-2 mb-5">
          <nuxt-link class="py-2 mx-2 dark:text-white border-b dark:border-white" :to="page.path">{{
            page.title
          }}</nuxt-link>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      pages: []
    }
  },
  async fetch() {
    this.pages = await this.$content('pages', { deep: true }).fetch()
  }
}
</script>
