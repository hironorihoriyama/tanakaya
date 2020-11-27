<template>
  <footer class="ft">
    <div class="ft_wp">
      <div class="ft_l">
        <Logo />
      </div>
      <div class="ft_r">
        <address class="ft_ad">
          奈良県桜井市初瀬748番地（〒633-0112）<br>
          TEL：0744-47-7015（代）<br>
          FAX：0744-47-7548<br>
          Mail：hase.tanakaya@gmail.com
        </address>
        <ul class="ft_lnks">
          <li><a href="/"><img src="~/assets/img/fb.svg" alt="fb">Facebook</a></li>
          <li><a href="/"><img src="~/assets/img/ig.svg" alt="ig">Instagram</a></li>
          <li><a href="/"><img src="~/assets/img/en.svg" alt="en">English</a></li>
        </ul>
      </div>
    </div>
  </footer>
</template>

<style lang="sass">
@import '~assets/scss/_variable.scss';
@import '~assets/scss/_mixin.scss';
.ft
  @include wf-gen()
  background-color: $key
  padding: 48px 36px
  &_wp
    max-width: 983px
    margin-right: auto
    margin-left: auto
    display: flex
    @include mediaQuery-down(sm)
      flex-direction: column
  &_r
    display: flex
    margin-left: 110px
    @include mediaQuery-down(md)
      flex-direction: column
    @include mediaQuery-down(sm)
      margin-left: 0
      margin-top: 32px
  &_ad
    font-size: 16px
    line-height: 1.6875
    color: $white
    font-style: normal
  &_lnks
    margin-left: 82px
    padding: 0
    list-style: none
    @include mediaQuery-down(md)
      margin-left: 0
      margin-top: 32px
    & a
      font-size: 16px
      color: $white
      text-decoration: none
    & img
      margin-right: 5px
</style>