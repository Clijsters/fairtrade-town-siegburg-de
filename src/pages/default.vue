<template>
  <div id="app" class="app is__center">
    <navigation />
    <hero />
    <about />
    <projects />
    <contact />
    <foot />
  </div>
</template>

<script>
import navigation from '@/components/Navigation'
import hero from '@/components/Hero'
import about from '@/components/About'
import projects from '@/components/Projects'
import contact from '@/components/Contact'
import foot from '@/components/Foot'
export default {
  name: 'App',
  components: {
    navigation,
    hero,
    about,
    projects,
    contact,
    foot
  }
}
</script>
