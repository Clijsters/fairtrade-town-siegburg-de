<template>
  <section id="hero" class="hero">
    <div class="hero__graylayer container--fluid ">
      <div class="hero__container">
        <h1 class="hero__hello">
        </h1>
        <p class="hero__info1">
        </p>
        <a v-scroll-to="{ el: '#about', offset: -40 }" class="hero__more" href="#">
          <p>{{ $t("hero.more") }}</p>
          <span class="hero__arrow" />
        </a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  mounted () {
    this.setHeroHeight()
    window.addEventListener('resize', this.setHeroHeight)
  },
  methods: {
    /**
      Fixes incorrect 100vh on mobile clients.
    */
    setHeroHeight () {
      // document.getElementById('hero').style.height = `${window.innerHeight}px`
    }
  },
  destroy () {
    window.removeEventListener('resize', this.setHeroHeight)
  }
}
</script>
