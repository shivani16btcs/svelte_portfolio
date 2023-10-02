<script>
	import { onMount } from 'svelte';
	import Typed from 'typed.js';
  import girlIMage from '$lib/images/girl_typing_transparent.gif';

	let typed;

	onMount(() => {
		const strings = ['I like <b>Html</b>', 'I love <b>JavaScript</b>', 'I am <b>Web Developer</b>'];

		const options = {
			strings: strings,
			typeSpeed: 50,
			backSpeed: 50,
            loop:true
		};

		// Initialize Typed.js
		typed = new Typed('.typing', options);
	});
</script>

<style>
 
    .terminal {
      font-family: 'Courier New', monospace;
      background-color: #0a0a0a;
      color: #CCCCCC;
      padding: 2rem;
      border: 2px solid #1e3551;
    }
  </style>
  
  <div class="min-h-screen flex items-center justify-center">
    <div class="terminal w-full h-screen text-xl">
      <p>Hello World! I am Shivani </p>
      <span class="typing"></span>
    </div>
    <img src={girlIMage} alt="Girl" class="absolute bottom-0 right-0 max-h-96 max-w-96" />
  </div>


