<script>
	import { onMount } from 'svelte';
	import Typed from 'typed.js';
	import girlImage from '$lib/images/girl_typing_transparent.gif';

	let typed;

	onMount(() => {
		const strings = [
			'<b>Web Developer</b>',
			'<b>Frontend Specialist</b>',
			'<b>Problem Solver</b>',
			'<b>Tech Explorer</b>'
		];

		const options = {
			strings: strings,
			typeSpeed: 50,
			backSpeed: 50,
			loop: true
		};

		// Initialize Typed.js
		typed = new Typed('.typing', options);
	});
</script>

<div class="min-h-screen flex items-center justify-center">
	<div class="terminal w-full h-screen text-xl">
		<div class="mt-20 ml-5">
			<p>Hello World! I am Shivani</p>
			<p>
				I am a passionate <span class="typing" />.
			</p>
			<p>Let's create something impactful together!</p>
		</div>
	</div>
	<img src={girlImage} alt="Girl typing on laptop" class="girl-img absolute bottom-0 right-0 max-h-96 max-w-96" />
</div>

<style>
	.terminal {
		background-color: #0a0a0a;
		color: #cccccc;
		padding: 2rem;
	}
	.girl-img {
		filter: drop-shadow(1px 1px 20px white);
	}
</style>