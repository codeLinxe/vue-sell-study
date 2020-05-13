<template>
  <div id="app" @touchmove.prevent>
    <v-header :seller="seller"></v-header>
    <header-detail :seller="seller"></header-detail>
  </div>
</template>

<script>
  import VHeader from 'components/v-header/v-header'
  import HeaderDetail from 'components/header-detail/header-detail'
  import { getSeller } from 'api/index'

  export default {
    name: 'App',
    components: {
      VHeader,
      HeaderDetail
    },
    data() {
      return {
        seller: {}
      }
    },
    created() {
      this._getSeller()
    },
    methods: {
      _getSeller() {
        getSeller().then((seller) => {
          this.seller = seller
        })
      }
    }
  }
</script>

<style lang="stylus">
</style>
