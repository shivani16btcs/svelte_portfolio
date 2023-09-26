<script>
	import Header from './Header.svelte';
	import './styles.css';
	import "../app.css";
</script>

<div class="app">
	<Header />

	<main>
		<slot />
	</main>
</div>

