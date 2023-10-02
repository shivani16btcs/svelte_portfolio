<script>
    import SnackIt from '$lib/images/snackIt.png';
	import JSGame from '$lib/images/js-game.png';
	import GymSIte from '$lib/images/gym_site.png';
	import multiColumnSort from '$lib/images/multicolumn2.png';

	
</script>

<section class="projects" id="projects">
	<div class="max-width">
		<h2 class="title">My Projects</h2>
		<div class="carousel owl-carousel">
            <a href="https://snack-it.vercel.app/home" target="_blank">
			<div class="card">
				<div class="box">
					<img src={SnackIt} alt="" />
					<div class="text">Snack It</div>
					<p>Instant snack nutrition details from photos – Snack smarter!.</p>
				</div>
			</div>
            </a>
            <a href="https://shivani16btcs.github.io/javascript-game/" target="_blank">
                <div class="card">
                    <div class="box">
                        <img src={JSGame} alt="" />
                        <div class="text">Game</div>
                        <p>Red vs. Blue: A 6-round JavaScript showdown. Who'll come out on top?</p>
                    </div>
                </div>
            </a>
			
            <a href="https://gym-site-github-io.vercel.app/" target="_blank">
                <div class="card">
                    <div class="box">
                        <img src={GymSIte} alt="" />
                        <div class="text">Gym Website</div>
                        <p>Designed and developed a dynamic website for a gym</p>
                    </div>
                </div>
            </a>
			<a href="https://insights.daffodilsw.com/blog/multi-column-sort-in-angularjs" target="_blank">
                <div class="card">
                    <div class="box">
                        <img src={multiColumnSort} alt="" />
                        <div class="text">Multicolumn sort Blog and sample</div>
                        <p>
                            implemented AngularJS multi-column sorting with extensive documentation and code samples, showcased on Daffodil's platform.
                        </p>
                    </div>
                </div>
            </a>
			
		</div>
	</div>
</section>

<style>
	.projects {
		padding: 100px 0;
	}
</style>
