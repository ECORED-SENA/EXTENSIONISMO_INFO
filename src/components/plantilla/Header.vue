<template lang="pug">
header.header
  .container
    .row.align-items-center.justify-content-between
      .col.col-sm-auto.d-flex.align-items-center.justify-content-between.justify-content-sm-star
        img.header__logo.me-sm-5(src="@/assets/template/logo-sena-naranja.svg")

</template>

<script>
import { global } from '../../config/global'
import mixins from '../../mixins/plantillaMixins'
export default {
  name: 'Header',
  mixins: [mixins],
  data: () => ({
    globalData: global,
  }),
  computed: {
    isInicio() {
      return this.$route.name === 'inicio'
    },
    menuOpen() {
      return this.$store.getters.isMenuOpen
    },
  },
  methods: {
    toggleMenu(newVal) {
      this.$store.dispatch('toggleMenu', newVal)
    },
  },
}
</script>

<style lang="sass" scoped>
.header
  position: sticky
  top: 0
  padding-top: 10px
  padding-bottom: 10px
  background-color: $white
  z-index: 10010
  line-height: 1.1em
  &__logo
    width: 50px


.header__menu
  cursor: pointer
  span
    font-size: 0.7em
    display: block
    line-height: 1em
    text-align: center
    color: $color-sistema-a
  &__btn
    width: 30px
    height: 30px
    position: relative
    margin-bottom: 4px
    .line-1,.line-2,.line-3
      height: 4px
      width: 30px
      background-color: $color-sistema-a
      transform-origin: center center
      position: absolute
      left: 0
      border-radius: 2px
    .line-1
      top: 4px
      animation: line-1-inactive 0.5s ease-in-out forwards
    .line-2
      top: 13px
      animation: line-2-inactive 0.5s ease-in-out forwards
    .line-3
      top: 22px
      animation: line-3-inactive 0.5s ease-in-out forwards
    &:hover
      cursor: pointer

    &--open
      .line-1
        animation: line-1-active 0.5s ease-in-out forwards
      .line-2
        animation: line-2-active 0.5s ease-in-out forwards
      .line-3
        animation: line-3-active 0.5s ease-in-out forwards

@keyframes line-1-active
  0%
    transform: translate(0, 0) rotate(0)
  50%
    transform: translate(0, 9px) rotate(0)
  100%
    transform: translate(0, 9px) rotate(45deg)

@keyframes line-2-active
  0%
    transform: scale(1)
  100%
    transform: scale(0)

@keyframes line-3-active
  0%
    transform: translate(0, 0) rotate(0)
  50%
    transform: translate(0, -9px) rotate(0)
  100%
    transform: translate(0, -9px) rotate(-45deg)

@keyframes line-1-inactive
  0%
    transform: translate(0, 9px) rotate(45deg)
  50%
    transform: translate(0, 9px) rotate(0)
  100%
    transform: translate(0, 0) rotate(0)

@keyframes line-2-inactive
  0%
    transform: scale(0)
  100%
    transform: scale(1)

@keyframes line-3-inactive
  0%
    transform: translate(0, -9px) rotate(-45deg)
  50%
    transform: translate(0, -9px) rotate(0)
  100%
    transform: translate(0, 0) rotate(0)
</style>
