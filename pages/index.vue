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
      <h2 class="text-center text-xl leading-normal">
        <a
          class="dark:text-white underline"
          rel="noopener"
          target="_blank"
          href="https://www.amazon.co.uk/dp/1916883605?ref_=pe_3052080_397514860"
          ><strong>Now Available!</strong> <br />
          Click to purchase via Amazon</a
        >
      </h2>
      <a
        class="w-full sm:w-1/2"
        href="https://www.amazon.co.uk/dp/1916883605?ref_=pe_3052080_397514860"
        rel="noopener"
        target="_blank"
        ><img src="~/assets/images/book-cover.png" alt="Click to purchase"
      /></a>
      <h2 class="subtitle text-center text-lg leading-normal">
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
