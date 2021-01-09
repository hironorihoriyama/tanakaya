<template>
  <div class="lg" :class="{ 'lg-gray': gray}">
    <div class="lg_w">
      <img src="~/assets/img/logo.svg" alt="logo">
      <img src="~/assets/img/logo-lead.svg" alt="logo-lead" class="lg_lead">
    </div>
    <div class="lg_g">
      <img src="~/assets/img/logo-g.svg" alt="logo-g">
      <img src="~/assets/img/logo-lead-g.svg" alt="logo-lead-g" class="lg_lead">
    </div>
  </div>
</template>

<script>
export default {
  props: {
    gray: { type: Boolean, default: false },
  }
}
</script>

<style lang="sass">
.lg
  &_g
    display: none
  &.lg-gray
    & .lg_w
      display: none
    & .lg_g
      display: block
  &_lead
    margin-left: 18.3px
</style>