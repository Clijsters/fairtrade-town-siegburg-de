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

      <ul class="about__social row row--multiline">
        <li class="column--3 column-mobile--6 contact__item">
          <a href="https://siegburg.de/stadtleben-aktuelles/newsletter/anmelden/index.html" target="_blank" rel="nofollow">
            <img class="contact__image" src="../assets/mail.png" alt="mail-Logo">
            <p class="contact__image__description">Siegburg Aktuell</p>
          </a>
        </li>
        <li class="column--3 column-mobile--6 contact__item">
          <a href="https://www.instagram.com/kreisstadt_siegburg/?hl=de" target="_blank" rel="nofollow" >
            <img class="contact__image" src="../assets/instagram-logo.png" alt="mail-Logo">
            <p class="contact__image__description">Instagram</p>
          </a>
        </li>
        <li class="column--3 column-mobile--6 contact__item">
          <a href="https://www.facebook.com/kreisstadtsiegburg/" target="_blank" rel="nofollow">
            <img class="contact__image" src="../assets/facebook-logo.png" alt="Mail-Logo">
            <p class="contact__image__description">Facebook</p>
          </a>
        </li>
        <li class="column--3 column-mobile--6 contact__item">
          <a href="https://www.siegburg.de" target="_blank" rel="nofollow">
            <img class="contact__image" src="../assets/ftts-logo-weiss.png" alt="Mail-Logo">
            <p class="contact__image__description">siegburg.de</p>
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
