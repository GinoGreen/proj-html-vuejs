<template>
  <div id="app">
    <Header />
    <Main />
    <Footer :footerLists="footerLists" />
  </div>
</template>

<script>
import Footer from './components/Footer.vue'
import Header from './components/Header.vue'
import Main from './components/Main.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer

  },
  data() {
    return {
      footerLists: [
        {
          title: 'explore',
          voices: [
            'Start here',
            'Blog',
            'About us',
          ],
        },
        {
          title: '',
          voices: [
            'Success story',
            'Courses',
            'Contact us',
          ],
        },
        {
          title: 'information',
          voices: [
            'Membership',
            'Purchase guide',
            'Privacy policy',
            'Terms of services',
          ],
        },
      ]
    }
  }
}
</script>

<style lang="scss">
@import './assets/style/generals.scss';

</style>
