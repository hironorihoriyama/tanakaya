<template>
  <div class="top">
    <Mnu />
    <div :style="styleObject" class="top_kv">
      <p class="top_kv_msg">
        旅情を優しくつつみこみ、<br>
        日常を忘れゆっくりとお寛ぎください。
      </p>
    </div>
    <Clm>
      <div class="top_ab">
        <div class="top_ab_ld">
          <img src="~/assets/img/ttl1.svg" alt="ttl1">
          <p>
            奈良時代に創建された真言宗豊山派の総本山長谷寺。<br>
            その門前町にて昭和初期ごろに料理旅館田中屋は創業いたしました。<br>
            以来長谷寺や門前町とも深く関わりながら、今日まで至っております。
          </p>
        </div>
        <Btn class="top_ab_btn">
          <a href="#">より詳しく見る</a>
        </Btn>
      </div>
    </Clm>
    <div class="top_fdimg"></div>
    <Clm>
      <div class="top_fd">
        <img
          src="~/assets/img/tohu.jpg"
          srcset="~/assets/img/tohu.jpg 1x,~/assets/img/tohu@2x.jpg 2x"
          alt="ttl2"
        >
        <div class="top_fd_ld">
          <img src="~/assets/img/ttl2.svg" alt="ttl2">
          <p>
            地の季節の食材を使用した野菜の炊き合わせや天ぷら、伝統料理の茶粥や三輪素麺などをご堪能いただけます。<br>
            特に胡麻豆腐は田中屋の名物料理としてご好評をいただいております。
          </p>
          <Btn class="top_fd_btn">
            <a href="#">より詳しく見る</a>
          </Btn>
        </div>
      </div>
    </Clm>
    <div class="top_rmimg"></div>
    <div class="top_rm">
      <div class="top_rm_wp">
        <img src="~/assets/img/ttl3.svg" alt="ttl3">
        <div class="top_rm_wp_ss">
          <Swiper1 />
        </div>
        <div class="top_rm_btn_wp">
          <Btn class="top_rm_btn">
            <a href="#">より詳しく見る</a>
          </Btn>
        </div>
      </div>
    </div>
    <h2 class="top_map">交通アクセス</h2>
    <Gmap />
    <Clm>
      <div class="top_map_ad">
        <p><img src="~/assets/img/pin.svg" alt="pin">633-0112 奈良県桜井市初瀬748番地</p>
        <p><img src="~/assets/img/tel.svg" alt="tel">0744-47-7015（代）</p>
        <p><img src="~/assets/img/clk.svg" alt="clk">10:00-20:00</p>
      </div>
      <div class="top_map_msg">
        <div class="top_map_msg_wp">
          <h3>お車でお越しの方</h3>
          <p>当館隣に駐車場をご用意しております（x台分）のでご利用ください。</p>
        </div>
        <div class="top_map_msg_wp">
          <h3>鉄道でお越しの方</h3>
          <p>最寄り駅は近鉄大阪線「長谷寺駅」で、当館までは駅から徒歩で約20分です。</p>
        </div>
      </div>
    </Clm>
    <div class="top_ts">
      <div class="top_ts_wp">
        <img src="~/assets/img/ttl4.svg" alt="ttl4">
        <div class="top_ts_wp_ss">
          <Swiper2 />
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>

<script>
export default {
  data() {
    let innerHeight = 0
    if(process.browser) {
      innerHeight = window.innerHeight
    }
    return {
      styleObject: {
        minHeight: innerHeight + 'px'
      },
    }
  },
  methods: {
    handleResize: function() {
      this.styleObject.minHeight = window.innerHeight + 'px'
    },
  },
  mounted() {
    window.addEventListener('resize', this.handleResize)
  },
  beforeDestroy() {
    window.removeEventListener('resize', this.handleResize)
  },
}
</script>

<style lang="sass">
@import '~assets/scss/_variable.scss';
@import '~assets/scss/_mixin.scss';

.top
  @include wf-ten()
  &_kv
    color: $white
    background-image: url('~@/assets/img/kv1.jpg')
    @include retina
      background-image: url('~@/assets/img/kv1@2x.jpg')
    background-size: cover
    background-position: center
    display: flex
    align-items: center
    &_msg
      width: 70%
      max-width: 788.2px
      margin-right: auto
      margin-left: auto
      font-size: 24px
      line-height: 1.875
      text-shadow: 0 3px rgba(0, 0, 0, 16%)
  &_ab
    margin: 192px auto 143px auto
    width: 70%
    &_ld
      display: flex
      & p
        margin-left: 113px
        font-size: 16px
        line-height: 2.5
        color: $key-txt
        @include wf-gen()
    &_btn
      margin-top: 134px
      margin-left: auto
      margin-right: auto
  &_fdimg
    height: 450px
    background-size: cover
    background-position: center
    background-image: url('~@/assets/img/fdimg.jpg')
    @include retina
      background-image: url('~@/assets/img/fdimg@2x.jpg')
  &_fd
    margin: 240px auto
    width: 80%
    display: flex
    &_ld
      margin-left: 120px
      & p
        margin-top: 43px
        font-size: 16px
        line-height: 2.5
        color: $key-txt
        @include wf-gen()
    &_btn
      margin-top: 99px
      margin-left: auto
      margin-right: auto
  &_rmimg
    height: 450px
    background-size: cover
    background-position: center
    background-image: url('~@/assets/img/rmimg.jpg')
    @include retina
      background-image: url('~@/assets/img/rmimg@2x.jpg')
  &_rm
    display: flex
    &_wp
      height: 915px
      width: 100%
      position: relative
      & img
        position: absolute
        top: 240px
        left: 177px
      &_ss
        position: absolute
        top: 240px
        right: 0
        width: 75%
        overflow: hidden
    &_btn
      margin-left: auto
      margin-right: auto
      &_wp
        position: absolute
        width: 100%
        top: 744px
  &_map
    font-size: 30px
    letter-spacing: 0.1
    font-weight: normal
    text-align: center
    margin-bottom: 40px
    &_ad
      width: 60%
      margin-top: 44px
      margin-left: auto
      margin-right: auto
      display: flex
      & p
        @include wf-gen()
        display: flex
        align-items: center
        font-size: 16px
        margin-right: 50px
        color: $key-txt
        &:last-of-type
          margin-right: 0
        & img
          margin-right: 8px
    &_msg
      margin: 90px auto 98px auto
      display: flex
      justify-content: space-between
      width: 70%
      &_wp
        background-color: #F4ECE1
        width: 336px
        height: 187px
        padding: 21px 23px 44px 23px
        text-align: center
        border-radius: 15px
        & h3
          font-size: 24px
          font-weight: normal
        & p
          @include wf-gen()
          color: $key-txt
          font-size: 16px
          margin-top: 23px
  &_ts
    display: flex
    &_wp
      height: 672px
      width: 100%
      background-color: $key-bg
      position: relative
      & img
        position: absolute
        top: 125px
        left: 177px
      &_ss
        position: absolute
        top: 125px
        right: 0
        width: 75%
        overflow: hidden
</style>