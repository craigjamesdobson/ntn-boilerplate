<template>
  <main>
    <section class="self-center flex flex-col flex-1 items-center justify-center">
      <h1 class="title text-center font-cursive leading-normal text-5xl md:text-6xl uppercase tracking-widest">
        The
        <br />
        Girl
        <br />
        Beneath
        <br />
        the
        <br />
        Willow
      </h1>
      <h2 class="subtitle text-center text-base leading-normal">
        The debut novel from
        <br />
        <span class="uppercase font-black text-xl tracking-widest">Rebecca Louise Dobson</span>
        <div class="flex justify-center mt-4 text-center">
          <a href="https://www.instagram.com/rebeccalouise_writes" rel="external nofollow" target="_blank">
            <component
              :is="`icon-instagram`"
              class="icon w-10 h-10 mx-2 fill-current"
              title="Toggle background color"
              tabindex="0"
            />
          </a>
          <a href="https://www.facebook.com/Rebeccalouisewrites" rel="external nofollow" target="_blank">
            <component
              :is="`icon-facebook`"
              class="icon w-10 h-10 mx-2 fill-current"
              title="Toggle background color"
              tabindex="0"
            />
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
  }
}
</script>

<style lang="postcss">
.icon {
  color: var(--text);
}
</style>
