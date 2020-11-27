<template>
  <div
    class="btn"
    :class="{ 'btn-bl': bl, 'btn-tl': tl, 'btn-ig': ig }"
  >
    <slot />
  </div>
</template>

<script>
export default {
  props: {
    bl: { type: Boolean, default: false },
    tl: { type: Boolean, default: false },
    ig: { type: Boolean, default: false },
  },
}
</script>

<style lang="sass">
@import '~assets/scss/_variable.scss';
@import '~assets/scss/_mixin.scss';

.btn
  @include wf-ten()
  width: 178px
  height: 48px
  border: 2px solid $key
  border-radius: 4px
  padding: 12px 31px
  background-color: $white
  &:hover
    background-color: $key
    & a
      color: $white
  & a
    display: flex
    justify-content: center
    align-items: center
    font-size: 16px
    height: 100%
    text-decoration: none
    color: $key
  &-bl a
    background-color: $gray-bg
    &:hover
      background-color: $white 

</style>
