<style lang="sass" global>
@import '../style/variables.sass'

html
  font-family: $font-default
  font-size: 24px
  color: hsl(0, 0%, 21%)
  word-spacing: 1px
  -ms-text-size-adjust: 100%
  -webkit-text-size-adjust: 100%
  -moz-osx-font-smoothing: grayscale
  -webkit-font-smoothing: antialiased
  box-sizing: border-box

*, *:before, *:after
  box-sizing: border-box
  margin: 0
  padding: 0

@media screen and (max-width: $breakpoint-tablet)
  html
    font-size: 20px

@media screen and (max-width: $breakpoint-mobile)
  html
    font-size: 16px

</style>

<main>
	<slot></slot>
</main>