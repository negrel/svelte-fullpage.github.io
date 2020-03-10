<svelte:head>
	<title>Svelte - Fullpage.js component</title>
</svelte:head>

<div>
	<svelte:component this={Fullpage} {options}>
		<div id="section-1" class="section" data-anchor="page1">
			<div class="title">
				<h1>svelte-fullpage.js</h1>
				<h2>Svelte wrapper for the fullpage.js library.</h2>
			</div>
			<Shields />
		</div>
		<div id="section-2" class="section" data-anchor="page2">
			<div>
				<h1>Easy !</h1>
				<h2>The power of fullpage.js in a simple to use svelte component.</h2>
			</div>
			<Example />
		</div>
		<div id="section-3" class="section" data-anchor="page3">
			<Gif />
			<span>Coded with love by <a href="https://negrel.dev/">Alexander Negrel</a></span>
		</div>
	</svelte:component>
</div>

<script>
import { onMount } from 'svelte';

import Example from './_index/example-frame.svelte';
import Gif from './_index/gif-frame.svelte';
import Shields from './_index/Shields.svelte';

// Fullpage svelte component
let Fullpage;

onMount(async () => {
	const module = await import('svelte-fullpage.js');
  Fullpage = module.default;
});

const options = {
	anchors: ['page1', 'page2', 'page3'],
	licenseKey: 'your license key'
};
</script>

<style lang="sass">
@import '../style/variables.sass'

*
	user-select: none

h1
	white-space: nowrap
	font-size: 8vw

.section
	position: relative
	color: $white

	& .title
		position: absolute
		top: 50%
		left: 50%
		transform: translate(-50%, -50%)

		& h2
			font-size: calc(1vw + 2.5vh)
			opacity: .75

#section

	&-1
		background-color: #ff5f45
		text-align: center

		& :global(.shields)
			position: absolute
			bottom: 2.5%
			left: 50%
			transform: translateX(-50%)

	&-2
		background-color: #0798ec
		padding: calc(10vh - 5vw) 5vw

		& h2
			font-size: calc(1vw + 2.5vh)
			opacity: .75

		& :global(.mac-os-frame)
			max-width: 90vw
			font-size: .8em
			margin-top: 1em


	&-3
		background-color: #fec401

		& span
			position: absolute
			bottom: 2.5%
			left: 50%
			transform: translateX(-50%)

		& a
			color: $white
</style>