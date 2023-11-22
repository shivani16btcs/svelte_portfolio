<script>
	import profileImage from '$lib/images/Screenshot_2018-06-10-18-13-59.jpg';
	import helloWave from '$lib/images/Hello_wave.gif'
</script>

<!-- <div class="bg-black text-green-500 p-8 text-center flex flex-col items-center">
	<h1 class="text-4xl font-bold mb-4">About Me</h1>
	<div class="mb-4">
		<img
			src={girlIMage}
			alt="About Me GIF"
			class="mx-auto rounded-full max-w-sm shadow-lg transform hover:scale-105 transition-transform duration-300"
		/>
	</div>
	<p class="text-lg mb-6">Frontend Engineer with 4 Years of Experience</p>
	<button
		class="bg-green-500 hover:bg-green-600 text-black font-bold py-2 px-4 rounded-full transition duration-300 ease-in-out"
		on:click={startAnimation}
	>
		Click to Animate
	</button>
	<p
		class="{animate
			? 'opacity-100 transform translate-y-0 transition duration-500'
			: 'opacity-0 transform -translate-y-4 transition duration-300'} text-left mx-4 mt-6"
	>
		I am a passionate frontend engineer with a strong background in web development. Over the past 4
		years, I have worked on various projects, creating beautiful and user-friendly web interfaces.
		My expertise includes HTML, CSS, JavaScript, and modern frontend frameworks.
	</p>
</div> -->




<section class="about" id="about">
	<div class="max-width">
		<h2 class="title">About</h2>
		<div class="about-content">
			<div class="column left ">
				<img src={profileImage} alt="profileImage" class="profile-img" />
			</div>
			<div class="column right">
				<div class="text flex">Hey there,
					<img src={helloWave} alt="profileImage" class="w-8 h-8" />
				</div>
				<p class="text-gray-700 text-lg leading-relaxed">
					I'm Shivani Yadav, a web developer based in Uttar Pradesh, India. Coding and design are my
					creative playground.
				</p>
				<p class="mt-2 text-gray-700 text-lg leading-relaxed">
					I'm a passionate developer with a strong background in web application development, dedicated to crafting high-quality solutions that surpass expectations.
				</p>
				<br />
				<p>Let's team up and bring your digital vision to reality!</p>
				<a href="https://www.linkedin.com/in/shivani-yadav-abc/" target="blank"
					>Connect on LinkedIn</a
				>
			</div>
		</div>
	</div>
</section>


<style>
  .about{
    padding:100px 0;
  }

</style>


