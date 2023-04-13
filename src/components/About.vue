<template>
  <section id="about" class="about container--fluid">
    <div class="about__container__hello container--fluid">
      <h2 class="about__hello">
        {{ $t("about.hello") }}
      </h2>
    </div>
    <div class="about__container container--fluid">
      <p class="about__info1">
        {{ $t("about.info1") }}
      </p>

      <ul class="about__social row">
        <li class="column--3 contact__item">
          <a href="#" target="_blank" rel="nofollow">
            <img class="contact__image" src="../assets/linkedin.png" alt="LinkedIn-Logo">
            <p class="contact__image__description">{{ $t("contact.linkedin") }}</p>
          </a>
        </li>
        <li class="column--3 contact__item">
          <a href="#" target="_blank" rel="nofollow" >
            <img class="contact__image" src="../assets/github.png" alt="GitHub-Logo">
            <p class="contact__image__description">{{ $t("contact.github") }}</p>
          </a>
        </li>
        <li class="column--3 contact__item">
          <a href="#" target="_blank" rel="nofollow">
            <img class="contact__image" src="../assets/mail.png" alt="Mail-Logo">
            <p class="contact__image__description">{{ $t("contact.mail") }}</p>
          </a>
        </li>
        <li class="column--3 contact__item">
          <a href="#" target="_blank" rel="nofollow">
            <img class="contact__image" src="../assets/mail.png" alt="Mail-Logo">
            <p class="contact__image__description">{{ $t("contact.mail") }}</p>
          </a>
        </li>
      </ul>
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
