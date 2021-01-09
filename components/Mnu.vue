<template>
  <header
    class="mnu"
    :class="{ 'mnu_cng': scrollY > 81 }"
  >
    <div class="mnu_wp">
      <div class="mnu_ttl">
        <Logo :gray="gray" />
      </div>
      <div class="mnu_btn_wp">
        <a
          class="mnu_btn"
          :class="{ active: tgl }"
          @click="tgl=!tgl"
          href="#"
        >
          <span></span>
          <span></span>
          <span></span>
        </a>
      </div>
      <ul
        class="mnu_ls"
        :class="{ active: tgl }"
      >
        <li><nuxt-link to="/about" :class="{ 'mnu-gray': gray }">田中屋について</nuxt-link></li>
        <li><nuxt-link to="/food" :class="{ 'mnu-gray': gray }">お料理</nuxt-link></li>
        <li><a href="http://cc-soluna.com/#top_cmp" :class="{ 'mnu-gray': gray }">お部屋</a></li>
        <li><a href="/" class="mnu_ls_rsv" :class="{ 'mnu-gray': gray }">ご予約</a></li>
        <li><a href="/" :class="{ 'mnu-gray': gray }">日/En</a></li>
      </ul>
    </div>
  </header>
</template>

<script>
export default {
  props: {
    gray: { type: Boolean, default: false },
  },
  data: function() {
    return {
      tgl: false,
      scrollY: 0
    }
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll)
  },
  methods: {
    handleScroll() {
      this.scrollY = window.scrollY
    }
  }
}
</script>

<style　lang="sass">
@import '~assets/scss/_variable.scss';
@import '~assets/scss/_mixin.scss';
.mnu
  @include wf-ten()
  z-index: 2
  position: fixed
  top: 0
  width: 100%
  padding-right: 80px
  padding-left: 73px
  transition: background-color 1s
  @include mediaQuery-down(sm)
    padding-left: 36px
    padding-right: 36px
  &_cng
    background-color: black
  &_wp
    position: relative
    max-width: 1126px
    margin-right: auto
    margin-left: auto
    height: 81px
    display: flex
    align-items: center
    justify-content: space-between
  &_ttl
  &_btn, &_btn span
    display: inline-block
    transition: all .4s
    box-sizing: border-box
  &_btn
    position: relative
    width: 40px
    height: 34px
    &:focus
      outline: none
      -webkit-tap-highlight-color: rgba(0, 0, 0, 0)
    &_wp
      display: none
      @include mediaQuery-down(md)
        display: block
        z-index: 11
    & span
      position: absolute
      left: 0
      width: 100%
      height: 4px
      background-color: $white
      border-radius: 4px
      &:nth-of-type(1)
        top: 0
      &:nth-of-type(2)
        top: 15px
      &:nth-of-type(3)
        bottom: 0
    &.active span:nth-of-type(1)
      -webkit-transform: translateY(15px) rotate(-45deg)
      transform: translateY(15px) rotate(-45deg)
    &.active span:nth-of-type(2)
      opacity: 0
    &.active span:nth-of-type(3)
      -webkit-transform: translateY(-15px) rotate(45deg)
      transform: translateY(-15px) rotate(45deg)
  &_ls
    list-style: none
    padding: 0
    display: flex
    @include mediaQuery-down(md)
      display: none
    &_rsv
      padding: 3px 8px
      border: 1px solid $white
      border-radius: 2px
      &.mnu-gray
        border-color: $key
    & li
      font-size: 14px
      margin-left: 33px
      &:last-of-type
        margin-bottom: 0
      & a
        text-decoration: none
        color: $white
        &.mnu-gray
          color: $key
    &.active
      z-index: 10
      display: block
      position: fixed
      top: 0
      left: 0
      width: 100%
      height: 100%
      padding-top: 180px
      background-color: rgba(0, 0, 0, 0.5)
      & li
        font-size: 24px
        text-align: center
        margin-left: 0
        margin-bottom: 30px
</style>