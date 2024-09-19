<script>
	import profileImage from '$lib/images/Screenshot_2018-06-10-18-13-59.jpg';
	import helloWave from '$lib/images/Hello_wave.gif';
	import Button3D from './Button3D.svelte';
</script>

<section class="about" id="about">
	<div class="max-width">
		<h2 class="text-4xl font-bold text-center mb-12 text-gray-900">About Me</h2>
		<div class="about-content">
			<div class="column left text-center md:text-left">
				<img
					src={profileImage}
					alt="Shivani Yadav"
					class="profile-img w-60 h-60 rounded-full mx-auto md:mx-0 shadow-lg border-4 border-white"
				/>
			</div>
			<div class="column right">
				<div class="text flex">
					Hey there,
					<img src={helloWave} alt="profileImage" class="w-8 h-8" />
				</div>
				<p class="text-gray-700 text-lg leading-relaxed">
					I'm Shivani Yadav, a web developer based in Uttar Pradesh, India. Coding and design are my
					creative playground.
				</p>
				<p class="mt-2 text-gray-700 text-lg leading-relaxed">
					I'm a passionate developer with a strong background in web application development,
					dedicated to crafting high-quality solutions that surpass expectations.
				</p>
				<br />
				<p>Let's team up and bring your digital vision to reality!</p>
				
				<Button3D text="Connect on LinkedIn" link="https://www.linkedin.com/in/shivani-yadav-abc/" />
			</div>
		</div>
	</div>
</section>

<style>
	.about {
		padding: 100px 0;
	}

	/* 3D button effect */
	.realistic-button {
		background: linear-gradient(145deg, #4a90e2, #357abd);
		color: white;
		padding: 12px 24px;
		border-radius: 12px;
		box-shadow: 6px 6px 12px rgba(0, 0, 0, 0.2), -4px -4px 8px rgba(255, 255, 255, 0.1);
		font-weight: 600;
		text-transform: uppercase;
		letter-spacing: 1px;
		transition: all 0.3s ease-in-out;
		display: inline-block;
		margin-top: 1.5rem;
	}

	.realistic-button:hover {
		background: linear-gradient(145deg, #357abd, #4a90e2);
		box-shadow: 8px 8px 16px rgba(0, 0, 0, 0.3), -6px -6px 12px rgba(255, 255, 255, 0.2);
		transform: translateY(-4px);
	}

	/* CSS */
	.button-6 {
		align-items: center;
		background-color: #ffffff;
		border: 1px solid rgba(0, 0, 0, 0.1);
		border-radius: 0.25rem;
		box-shadow: rgba(0, 0, 0, 0.02) 0 1px 3px 0;
		box-sizing: border-box;
		color: rgba(0, 0, 0, 0.85);
		cursor: pointer;
		display: inline-flex;
		font-family: system-ui, -apple-system, system-ui, 'Helvetica Neue', Helvetica, Arial, sans-serif;
		font-size: 16px;
		font-weight: 600;
		justify-content: center;
		line-height: 1.25;
		margin: 0;
		min-height: 3rem;
		padding: calc(0.875rem - 1px) calc(1.5rem - 1px);
		position: relative;
		text-decoration: none;
		transition: all 250ms;
		user-select: none;
		-webkit-user-select: none;
		touch-action: manipulation;
		vertical-align: baseline;
		width: auto;
	}

	.button-6:hover,
	.button-6:focus {
		border-color: rgba(0, 0, 0, 0.15);
		box-shadow: rgba(0, 0, 0, 0.1) 0 4px 12px;
		color: rgba(0, 0, 0, 0.65);
	}

	.button-6:hover {
		transform: translateY(-1px);
	}

	.button-6:active {
		background-color: #f0f0f1;
		border-color: rgba(0, 0, 0, 0.15);
		box-shadow: rgba(0, 0, 0, 0.06) 0 2px 4px;
		color: rgba(0, 0, 0, 0.65);
		transform: translateY(0);
	}
</style>
