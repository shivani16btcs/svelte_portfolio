<script>
	import SkillCards from '$lib/component/skills/SkillCard.svelte';
</script>


<section class="skills skill-head overflow-hidden" id="skills">
	<div class="max-width">
		<h2 class="title">My Skills</h2>
	</div>
	<div class="relative skill-content flex justify-center pb-32 mt-96 lg:mt-0  md:mb-10 lg:mb-20 mb-40">
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
