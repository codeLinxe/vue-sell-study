<template>
  <div id="app" @touchmove.prevent>
    <v-header :seller="seller"></v-header>
  </div>
</template>

<script>
  import VHeader from 'components/v-header/v-header'
  import { getSeller } from 'api/index'

  export default {
    name: 'App',
    components: {
      VHeader
    },
    data() {
      return {
        seller: {}
      }
    },
    created() {
      getSeller().then((seller) => {
        this.seller = seller
      })
    }
  }
</script>

<style lang="stylus">
</style>
