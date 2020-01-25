<script>
import MacOsFrame from '@/components/frame.svelte';
</script>

<a id="gif-frame" href="https://alvarotrigo.com/fullPage/" target="_blank">
  <MacOsFrame title="Official fullpage.js website">
    <img id="example-gif" src="fullpage.js.gif" alt="example gif">
  </MacOsFrame>
</a>

<style lang="sass">
#gif-frame
  position: absolute
  top: 10%
  left: 50%
  transform: translateX(-50%)
  text-decoration: none

#example-gif
  display: block
  max-height: 50vh
  max-width: 90vw
</style>