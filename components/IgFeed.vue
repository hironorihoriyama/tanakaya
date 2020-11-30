<template>
  <div class="ig">
    <img src="~/assets/img/ttl5.svg" alt="ttl5">
    <ul class="ig_fd">
      <li v-for="feed in igFeed" :key="feed.id"><img :src="feed.media_url"></li>
    </ul>
    <Btn :ig="true" class="ig_btn">
      <a href="#"><img src="~/assets/img/ig.svg" alt="ig">Instagram</a>
    </Btn>
  </div>
</template>

<script>
export default {
  data() {
    return {
      igFeed: null,
    }
  },
  methods: {
    async getIgFeed() {
      const target_url = process.env.API_IG
      const feed = await this.$axios.$get(target_url)
      this.igFeed = feed.media.data
    }
  },
  created() {
    this.getIgFeed()
  }
}
</script>

<style lang="sass">
@import '~assets/scss/_variable.scss';
@import '~assets/scss/_mixin.scss';

.ig
  text-align: center
  margin-top: 104px
  max-width: 950px
  margin-left: auto
  margin-right: auto
  @include mediaQuery-down(md)
    max-width: 620px
  &_fd
    margin-top: 62.5px
    padding-left: 0
    list-style: none
    display: flex
    justify-content: space-between
    flex-wrap: wrap
    & li
      width: 280px
      margin-right: 52px
      margin-bottom: 51px
      &:nth-of-type(3n)
        margin-right: 0
        @include mediaQuery-down(md)
          margin-right: 52px
      &:nth-of-type(2n)        
        @include mediaQuery-down(md)
          margin-right: 0
      & img
        width: 100%
  &_btn
    margin-left: auto
    margin-right: auto
    margin-top: 49px
    margin-bottom: 138px
    & img
      width: 27px
      margin-right: 12px
</style>