<script>
	import SkillCards from '$lib/component/skills/SkillCard.svelte';
</script>



<section class="skills skill-head" id="skills">
	<div class="max-width">
		<h2 class="title">My Skills</h2>
		<p
			class="{true
				? 'opacity-100 transform translate-y-0 transition duration-500'
				: 'opacity-0 transform -translate-y-4 transition duration-300'} text-left mx-4 mt-6"
		>
			I am well-versed in a wide range of web development technologies and tools, and I work with
			them daily to create seamless and engaging online experiences. My expertise includes:
		</p>
		
		
	</div>
	<div class="relative skill-content flex justify-center pb-32 mt-96 md:mt-36 lg:mt-0  md:mb-0 lg:mb-20 mb-40">
		<div class="abolute z-0 ">
			<SkillCards />
		</div>
	</div>
</section>


<style>
	.skill-head {
		padding: 100px 0;
	}
</style>
