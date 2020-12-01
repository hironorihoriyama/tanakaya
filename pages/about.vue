<template>
  <div class="ab">
    <Mnu />
    <div class="ab_kv"></div>
    <Clm>
      <div class="ab_ld">
        <div class="ab_ld_wp">
          <img src="~/assets/img/ttl6.svg" alt="ttl6">
          <p>
            「隠国（こもりく）の泊瀬（はつせ）」と万葉集にもうたわれる初瀬。<br>
            この地には真言宗豊山派の総本山長谷寺があり、西国三十三観音霊場第八番札所として多くの人々の信仰をあつめてきました。<br>
            そんな長谷寺から徒歩2分のところに料理旅館田中屋は営業しております。
          </p>
        </div>
      </div>
    </Clm>
    <div class="ab_his">
      <div class="ab_his_wp">
        <div class="ab_his_imgs">
          <img src="~/assets/img/subttl1.svg" alt="subttl1" class="ab_his_imgs_sttl">
          <img
            src="~/assets/img/hisimg.jpg"
            srcset="~/assets/img/hisimg.jpg 1x,~/assets/img/hisimg@2x.jpg 2x"
            alt="ttl2"
            class="ab_his_imgs_img"
          >
        </div>
      </div>
      <Clm>
        <div class="ab_his_txt">
          <img src="~/assets/img/ttl7.svg" alt="ttl7">
          <p>
            長谷寺の創建は奈良時代とされ、全国に末寺三千余ヶ寺、 檀信徒はおよそ三百万人といわれております。<br>
            また、四季を通じて桜や牡丹、紫陽花、もみじなどが美しく境内を彩ることから「花の御寺」とも呼ばれ、多くの観光客も訪れます。<br>
            田中屋では、長谷寺を訪れる観光客の皆様にお食事やお宿をご提供しているほか、長谷寺の行事などにおいて、精進料理の仕出しもさせていただいております。
          </p>
        </div>
      </Clm>
    </div>
    <Clm>
      <div class="ab_twn">
        <div class="ab_twn_l">
          <img src="~/assets/img/ttl8.svg" alt="ttl8">
          <p>
            長谷寺の開祖である徳道上人により安置された十一面観音像。<br>
            この観音さまの霊験はあらたかで、平安時代になると女性の参拝者が絶えず、震旦（中国）までも利益を施したといいます。<br>
            「蜻蛉日記」の作者である藤原道綱母や「更級日記」の作者である菅原孝標女もここを訪れたようです。<br>
            こうした歴史の中で、初瀬のまちが形づくられていきました。<br>
            初瀬の門前町において、田中屋は昭和の中頃より料理旅館としてスタート。自家製の胡麻豆腐など地元食材を使用したお料理を訪れる皆様に味わっていただいております。
          </p>
        </div>
        <div class="ab_twn_r">
          <img
            src="~/assets/img/twnimg1.jpg"
            srcset="~/assets/img/twnimg1.jpg 1x,~/assets/img/twnimg1@2x.jpg 2x"
            alt="ttl2"
          >
          <img
            src="~/assets/img/twnimg2.jpg"
            srcset="~/assets/img/twnimg2.jpg 1x,~/assets/img/twnimg2@2x.jpg 2x"
            alt="ttl2"
          >
          <img
            src="~/assets/img/twnimg3.jpg"
            srcset="~/assets/img/twnimg3.jpg 1x,~/assets/img/twnimg3@2x.jpg 2x"
            alt="ttl2"
          >
        </div>
      </div>
    </Clm>
    <div class="ab_kn">
      <Clm>
        <div class="ab_kn_wp">
          <img
            src="~/assets/img/knimg.jpg"
            srcset="~/assets/img/knimg.jpg 1x,~/assets/img/knimg@2x.jpg 2x"
            alt="ttl2"
            class="ab_kn_l"
          >
          <div class="ab_kn_r">
            <img src="~/assets/img/ttl9.svg" alt="ttl9">
            <p>
              長谷寺に縁のある観音様ですが、田中屋でも観音像を中庭に祀っております。<br>
              今日も田中屋を訪れるお客様を、優しい眼差しで見守っておられます。
            </p>
          </div>
        </div>
      </Clm>
    </div>
    <Footer />
  </div>
</template>

<style lang="sass">
@import '~assets/scss/_variable.scss';
@import '~assets/scss/_mixin.scss';

.ab
  @include wf-gen()
  &_kv
    height: 594px
    background-image: url('~@/assets/img/kv2.jpg')
    @include retina
      background-image: url('~@/assets/img/kv2@2x.jpg')
    background-size: cover
    background-position: center
  &_ld
    margin: 121px auto 419px auto
    width: 64%
    &_wp
      display: flex
      & p
        margin-left: 79px
        font-size: 16px
        line-height: 2.5
        color: $key-txt
  &_his
    background-color: $sub-bg
    position: relative
    &_wp
      width: 100%
      position: absolute
      top: -218.5px
    &_imgs
      position: relative
      max-width: 1168px
      margin-left: auto
      margin-right: auto
      text-align: center
      &_sttl
        position: absolute
        left: 0
      &_img
        max-width: 100%
    &_txt
      width: 56%
      margin-left: auto
      margin-right: auto
      padding-top: 300px
      padding-bottom: 132px
      & p
        margin-top: 50.5px
        font-size: 16px
        line-height: 2.5
        color: $key-txt
  &_twn
    width: 88%
    margin: 198px auto 80px auto
    display: flex
    justify-content: space-between
    &_l
      max-width: 545px
      & p
        margin-top: 86px
        font-size: 16px
        line-height: 2.5
        color: $key-txt
    &_r
      max-width: 326px
      & img
        margin-bottom: 46px
  &_kn
    width: 100%
    background-color: $sub-bg
    &_wp
      width: 81%
      margin-left: auto
      margin-right: auto
      padding-top: 110px
      padding-bottom: 124px
      display: flex
      align-items: center
      justify-content: space-between
    &_l
      max-width: 100%
    &_r
      max-width: 338px
      & p
        margin-top: 60px
        font-size: 16px
        line-height: 2.5
        color: $key-txt
</style>