<template>
  <div>
    <p class="nwtxt">
      イベントのお知らせやレポートのほか、<br>
      アトリエ宝来の利用者紹介や、関係者の紹介を記事にしています。
    </p>
    <Btn class="nwbtn" :bl="true"><a href="https://note.com/atelier_2020" target="_blank" rel="noopener noreferrer">お知らせ</a></Btn>
  </div>
</template>

<style lang="sass">
@import '~assets/scss/_variable.scss';
.nwtxt
  margin-top: 118px
  color: $gray-txt
  text-align: center
.nwbtn
  margin-top: 38px
  margin-right: auto
  margin-left: auto
</style>