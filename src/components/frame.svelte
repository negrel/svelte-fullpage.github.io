<script>
import MacOsFrame from 'svelte-mac-os-frame';

export let title = '';

let options = {
	headerStyle: { background: "#1C1D21", color: "whitesmoke" },
	bodyStyle: {},
	titleStyle: { color: 'whitesmoke', textShadow: 'unset' },
	title
}
</script>

<MacOsFrame {...options}>
  <slot />
</MacOsFrame>