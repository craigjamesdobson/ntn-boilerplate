<template>
  <main>
    <section class="self-center flex flex-col flex-1 items-center justify-center">
      <!-- <h1
        class="title text-center font-cursive leading-normal text-5xl md:text-6xl uppercase tracking-widest font-light"
      >
        The
        <br />
        Girl
        <br />
        Beneath
        <br />
        the
        <br />
        Willow
      </h1> -->
      <a class="w-full sm:w-1/2 lg:w-1/4" href=""
        ><img src="~/assets/images/book-cover.png" alt="Click to purchase"
      /></a>
      <h2 class="subtitle text-center text-base leading-normal">
        <div class="flex justify-center mt-4 text-center">
          <a href="https://www.instagram.com/rebeccalouise_writes" rel="external nofollow" target="_blank">
            <component :is="`icon-instagram`" class="icon w-8 h-8 mx-2 fill-current" tabindex="0" />
          </a>
          <a href="https://www.facebook.com/Rebeccalouisewrites" rel="external nofollow" target="_blank">
            <component :is="`icon-facebook`" class="icon w-8 h-8 mx-2 fill-current" tabindex="0" />
          </a>
        </div>
      </h2>
    </section>
  </main>
</template>

<script>
import IconInstagram from '~/components/icons/instagram.svg?inline'
import IconFacebook from '~/components/icons/facebook.svg?inline'

export default {
  components: {
    IconInstagram,
    IconFacebook
  },
  async asyncData({ $content, error }) {
    let pages
    try {
      pages = await $content('pages').fetch()
    } catch (e) {
      error({ message: 'Pages not found' })
    }
    return { pages }
  }
}
</script>

<style lang="postcss">
.icon {
  color: var(--text);
}
</style>
