<script>
import MacOsFrame from 'svelte-mac-os-frame';
</script>

<div id="gif-frame">
  <MacOsFrame title="example.gif">
    <img id="example-gif" src="https://raw.githubusercontent.com/Nergel3/svelte-fullpage.js/master/resources/example.gif" alt="example gif">
  </MacOsFrame>
</div>

<style lang="sass">
#gif-frame
  position: absolute
  top: 10%
  left: 50%
  transform: translateX(-50%)

#example-gif
  max-height: 50vh
  max-width: 90vw
</style>