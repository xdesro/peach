<template>
  <div class="root">
    <div class="container">
      <Header />
      <nuxt />
    </div>
  </div>
</template>
<script>
import Header from '~/components/Header'
export default {
  components: {
    Header
  },
  data() {
    return {
      colorPairs: [
        { base: '#E0D3E2', primary: '#7D1045' },
        { base: '#FFE03D', primary: '#260202' }
      ]
    }
  },
  mounted() {
    const getRandomPair = () => {
      return this.colorPairs[Math.floor(Math.random() * this.colorPairs.length)]
    }
    const randomPair = getRandomPair()
    this.$el.style.setProperty('--color-base', randomPair.base)
    this.$el.style.setProperty('--color-primary', randomPair.primary)
  }
}
</script>

<style lang="scss">
@import '~assets/scss/main.scss';
</style>
