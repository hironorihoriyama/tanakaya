<template>
  <div class="fd">
    <Mnu :gray="true" />
    <Clm>
      <img src="~/assets/img/ttl10.svg" alt="ttl10" class="fd_ttl">
      <p class="fd_ld">
        昭和初期から営業している老舗のお食事処です。<br>
        四季を感じるお料理や名物の胡麻豆腐をお楽しみいただけます。
      </p>
    </Clm>
    <div class="fd_img"></div>
    <Clm>
      <div class="fd_goma_wp">
        <div class="fd_goma">
          <img
            src="~/assets/img/gomaimg.jpg"
            srcset="~/assets/img/gomaimg.jpg 1x,~/assets/img/gomaimg@2x.jpg 2x"
            alt="ttl2"
            class="fd_goma_l"
          >
          <div class="fd_goma_r">
            <img src="~/assets/img/ttl11.svg" alt="ttl11">
            <p>
              奈良特産の金胡麻を使い、油が出るまで丹念にすりつぶしてだし汁と合わせ、吉野葛をまぜて固めます。ていねいに作られた胡麻豆腐は、豊かな胡麻の香りとやわらかな舌ざわりが特徴です。お店で食べたあと、持ち帰りを希望するお客様も多いです。<br>
              長谷寺から依頼されたのをきっかけに作りはじめた、胡麻豆腐が美味です。
            </p>
          </div>
        </div>
      </div>
      <div class="fd_siki">
        <div class="fd_siki_l">
          <img src="~/assets/img/ttl12.svg" alt="ttl12">
          <p>
            同じお料理でも季節に応じて使う食材を変えております。ぜひ田中屋にて、古都奈良の四季をご賞味ください。
          </p>
        </div>
        <img
          src="~/assets/img/sikiimg.jpg"
          srcset="~/assets/img/sikiimg.jpg 1x,~/assets/img/sikiimg@2x.jpg 2x"
          alt="ttl2"
          class="fd_siki_r"
        >
      </div>
      <div class="fd_rcm">
        <img src="~/assets/img/ttl13.svg" alt="ttl13">
        <div class="fd_rcm_mnus">
          <div class="fd_rcm_mnus_wp">
            <img
              src="~/assets/img/sampleimg.jpg"
              srcset="~/assets/img/sampleimg.jpg 1x,~/assets/img/sampleimg@2x.jpg 2x"
              alt="sampleimg"
            >
            <h3>胡麻豆腐</h3>
            <p>当店のおすすめ品で、ほのかにゴマの香りが漂い、口に入れると、ファーと溶けていくなめらかな舌ざわり。</p>
          </div>
          <div class="fd_rcm_mnus_wp">
            <img
              src="~/assets/img/sampleimg.jpg"
              srcset="~/assets/img/sampleimg.jpg 1x,~/assets/img/sampleimg@2x.jpg 2x"
              alt="sampleimg"
            >
            <h3>冷やしそうめん定食</h3>
            <p>奈良の三輪そうめんをぜひご堪能ください。</p>
          </div>
          <div class="fd_rcm_mnus_wp">
            <img
              src="~/assets/img/sampleimg.jpg"
              srcset="~/assets/img/sampleimg.jpg 1x,~/assets/img/sampleimg@2x.jpg 2x"
              alt="sampleimg"
            >
            <h3>山菜定食</h3>
            <p>地域のものを基本に、季節ごとに変わる旬の野菜を使った定食です。</p>
          </div>
        </div>
      </div>
    </Clm>
    <div class="fd_htl">
      <div class="fd_htl_img"></div>
      <img src="~/assets/img/ttl14.svg" alt="ttl14">
      <p>ご宿泊のお料理は、1階のお食事処にて召し上がっていただきます。</p>
    </div>
    <Clm>
      <div class="fd_grp">
        <img src="~/assets/img/ttl15.svg" alt="ttl15" class="fd_grp_l">
        <div class="fd_grp_r">
          <img
              src="~/assets/img/fdimg3.jpg"
              srcset="~/assets/img/fdimg3.jpg 1x,~/assets/img/fdimg3@2x.jpg 2x"
              alt="fdimg3"
            >
        </div>
      </div>
    </Clm>
    <Footer />
  </div>
</template>

<style lang="sass">
@import '~assets/scss/_variable.scss';
@import '~assets/scss/_mixin.scss';

.fd
  &_ttl
    margin-top: 185px
    margin-left: 71px
  &_ld
    @include wf-ten()
    width: 530px
    margin: 88px auto 124px auto
    font-size: 16px
    line-height: 2.5
  &_img
    height: 515px
    margin-left: 11%
    background-image: url('~@/assets/img/fdimg2.jpg')
    @include retina
      background-image: url('~@/assets/img/fdimg2@2x.jpg')
    background-size: cover
    background-position: center
  &_goma
    width: 90%
    margin: 172px auto 149.5px auto
    display: flex
    align-items: center
    justify-content: space-between
    &_l
      max-width: 100%
    &_r
      max-width: 644px
      & p
        margin-top: 60px
        font-size: 16px
        line-height: 2.5
        color: $key-txt
    &_wp:after
      content: ''
      display: block
      height: 1px
      width: 203px
      margin-left: auto
      margin-right: auto
      margin-bottom: 71.5px
      background-color: black
  &_siki
    position: relative
    &_l
      max-width: 808px
      padding: 121px 363px 83px 78px
      background-color: $sub-bg
      & p
        margin-top: 60px
        font-size: 16px
        line-height: 2.5
        color: $key-txt
    &_r
      position: absolute
      top: 101px
      left: 505px
    &:after
      content: ''
      display: block
      height: 1px
      width: 203px
      margin: 175.5px auto 101.5px auto
      background-color: black
  &_rcm
    margin-left: 71px
    margin-bottom: 123px
    &_mnus
      margin-top: 52px
      display: flex
      justify-content: space-between
      &_wp
        max-width: 315px
        & h3
          @include wf-ten()
          margin-top: 29px
          font-size: 24px
          line-height: 1.875
          color: $key
        & p
          @include wf-gen()
          margin-top: 16px
          font-size: 16px
          line-height: 1.5
          color: $key-txt
  &_htl
    background-color: $sub-bg
    padding-top: 124px
    padding-bottom: 210px
    position: relative
    &_img
      width: 77%
      height: 486px
      background-image: url('~@/assets/img/fdimg3.jpg')
      @include retina
        background-image: url('~@/assets/img/fdimg3@2x.jpg')
      background-size: cover
      background-position: center
    & img
      position: absolute
      top: 124px
      right: 14%
    & p
      position: absolute
      left: 11%
      bottom: 124px
      @include wf-gen()
      font-size: 16px
      line-height: 1.5
      color: $key-txt
  &_grp
    width: 87%
    margin-top: 124px
    margin-left: 104px
    display: flex
    align-items: flex-start
    &_l
      margin-right: 95px
</style>