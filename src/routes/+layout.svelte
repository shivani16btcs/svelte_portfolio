<script>
	import Header from '$lib/component/Header.svelte';
	import About from '$lib/component/About.svelte';
	import Projects from '$lib/component/Projects.svelte';
	import Contact from '$lib/component/Contact.svelte';
	import Home from '$lib/component/Home.svelte';
	import Service from '$lib/component/Service.svelte';
	import Skill from '$lib/component/skills/Skill.svelte';

	import './styles.css';
</script>

<main>
	<Header />
	<section id="home">
		<Home />
	</section>
	<section id="about">
		<About />
	</section>
	<section id="services">
		<Service />
	</section>
	<section id="skills">
		<Skill />
	</section>	
	<section id="projects">
		<Projects />
	</section>
	<section id="contact">
		<Contact />
	</section>
	<slot />
</main>
