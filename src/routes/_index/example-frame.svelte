<script>
import MacOsFrame from '@/components/frame.svelte';

import Highlight from 'svelte-highlight';
import { xml } from 'svelte-highlight/languages';
import { anOldHope } from 'svelte-highlight/styles';
</script>

<svelte:head>
	{@html anOldHope}
</svelte:head>

<MacOsFrame title="Example.svelte">
	<Highlight language={xml}>
		{`
<script>
	import Fullpage from 'svelte-fullpage.js';

	const options = {
		navigation: true,
		responsiveWidth: 700,
		anchors: ['home', 'about-us', 'contact'],
		parallax: true,
		onLeave: function(origin, destination, direction){
			console.log("Leaving section" + origin.index);
		}
	}
</script>

<Fullpage {options}>
	<div class="section">Section 1</div>
	<div class="section">Section 2</div>
	<div class="section">Section 3</div>
</Fullpage>
		`}
	</Highlight>
</MacOsFrame>

<style lang="sass" global>
.mac-os-frame
	&_body
		user-select: text
</style>