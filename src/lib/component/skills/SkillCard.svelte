<div class="content flex justify-center items-center">
	<div class="profile-skill-card">
		<div>
			<!-- <span id="sk1"></span> -->
			<label
				for="sk1"
				class="flex justify-center items-center transform transition-transform hover:scale-125"
			>
				<!-- smile svg  -->
				<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" width="33" height="33">
					<!-- Face -->
					<circle cx="50" cy="50" r="40" stroke="#094675" stroke-width="2" fill="transparent" />

					<!-- Left eye -->
					<circle cx="35" cy="40" r="5" fill="#094675" />

					<!-- Right eye -->
					<circle cx="65" cy="40" r="5" fill="#094675" />

					<!-- Mouth (a simple curve) -->
					<path d="M35 60 Q 50 75 65 60" fill="transparent" stroke="#1e3551" stroke-width="2" />
				</svg>
			</label>
			<ul class="skill-card skill-card1">
				<!-- <li class="sk-css"><span>C</span></li> -->
				<li class="sk-htm"><span>Html</span></li>
				<li class="sk-css"><span>CSS</span></li>
				<li class="sk-js"><span>Javascript</span></li>
				<li class="more">
					<input type="checkbox" id="more-len" /><label for="more-len" />
					<div>
						<span>c</span><span>c++</span><span>typescript</span><span>SCSS</span><span
							>SASS</span><span>Tailwind</span>
					</div>
				</li>
				
			</ul>
		</div>
		<div>
			<label
				for="sk2"
				class="flex justify-center items-center transform transition-transform hover:scale-125"
			>
				<!-- smile svg  -->
				<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" width="33" height="33">
					<!-- Face -->
					<circle cx="50" cy="50" r="40" stroke="#094675" stroke-width="2" fill="transparent" />

					<!-- Left eye -->
					<circle cx="35" cy="40" r="5" fill="#094675" />

					<!-- Right eye -->
					<circle cx="65" cy="40" r="5" fill="#094675" />

					<!-- Mouth (a simple curve) -->
					<path d="M35 60 Q 50 75 65 60" fill="transparent" stroke="#1e3551" stroke-width="2" />
				</svg>
			</label>
			<ul class="skill-card skill-card2">
				<li class="sk-ang"><span>Angular</span></li>
				<li class="sk-svel"><span>Svelte</span></li>
				<li class="sk-node"><span>Nodejs</span></li>
				<li class="more">
					<input type="checkbox" id="more-pro" /><label for="more-pro" />
					<div>
						<span>API</span><span>Express.js</span><span>SQL</span><span>REST</span><span
							>MongoDB</span
						><span>GIT</span>
					</div>
				</li>
			</ul>
		</div>
		<div>
			<label
				for="sk3"
				class="flex justify-center items-center transform transition-transform hover:scale-125"
			>
				<!-- smile svg  -->
				<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" width="33" height="33">
					<!-- Face -->
					<circle cx="50" cy="50" r="40" stroke="#094675" stroke-width="2" fill="transparent" />

					<!-- Left eye -->
					<circle cx="35" cy="40" r="5" fill="#094675" />

					<!-- Right eye -->
					<circle cx="65" cy="40" r="5" fill="#094675" />

					<!-- Mouth (a simple curve) -->
					<path d="M35 60 Q 50 75 65 60" fill="transparent" stroke="#1e3551" stroke-width="2" />
				</svg>
			</label>
			<ul class="skill-card skill-card3">
				<li class="sk-git"><span>GIT</span></li>
				<li class="sk-npm"><span>npm</span></li>
				<li class="sk-post"><span>Postman</span></li>
				<li class="more">
					<input type="checkbox" id="more-con" /><label for="more-con" />
					<div>
						<span>JIRA</span><span>TRELLO</span><span>CMS</span><span>Jenkins</span><span>Vercel</span>
						<span>GIT</span>
					</div>
				</li>
			</ul>
		</div>
	</div>
</div>

<style>
	/*** IN PROGRESS ***/

	@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500&display=swap');

	:root {
		--c1: #0e4976;
		--b2: #222;
		--b3: #333;
		--w1: #fff;
		--w2: #eee;
		--t1: all 0.5s ease 0s;
	}

	/* body {
		margin: 0;
		padding: 0;
		width: 100vw;
		height: 100vh;
		display: flex;
		align-items: center;
		justify-content: center;
		font-family: 'Roboto', sans-serif;
		font-size: 15px;
	}

	* {
		box-sizing: border-box;
	}

	*:before,
	*:after {
		box-sizing: border-box;
		content: '';
	} */

	.content {
		width: 80vw;
		background: #fff0;
	}

	.profile-skill-card {
		display: flex;
		top: 150px;
		position: relative;
		width: 100%;
		align-items: flex-start;
	}

	.profile-skill-card > div {
		width: 32%;
		margin-right: 3%;
		border-radius: 2px;
		position: relative;
	}

	ul.skill-card {
		width: 100%;
		position: relative;
		padding: 25px 35px;
		background: linear-gradient(
			0deg,
			var(--c1) 0 10px,
			var(--b2) 0 calc(100% - 10px),
			var(--c1) 0 100%
		);
		border-bottom-left-radius: 6px;
	}

	ul.skill-card:before {
		content: 'Codes';
		text-transform: capitalize;
		position: absolute;
		top: -75px;
		height: 50px;
		color: var(--w1);
		background-color: var(--b2);
		width: 100%;
		left: 0;
		padding: 15px 15px 0 0;
		text-align: end;
		font-weight: 500;
		z-index: 1;
		transition: var(--t1);
		font-size: 25px;
		line-height: 35px;
		transform: scaleY(1.65);
		border-radius: 6px;
	}

	ul.skill-card2:before {
		content: 'Web Stack';
	}

	ul.skill-card3:before {
		content: 'tools';
	}

	ul.skill-card:after {
		content: '';
		position: absolute;
		border: 40px solid #fff0;
		border-top-color: var(--b2);
		top: -30px;
		left: 10px;
		z-index: 0;
		transition: var(--t1);
		filter: drop-shadow(0 11px 0.1px var(--w1));
	}

	ul.skill-card:hover:before,
	label:hover + ul.skill-card:before,
	input:checked + label + ul.skill-card:before {
		transition: var(--t1);
		background-color: var(--c1);
		background-position: 0 50%;
	}

	ul.skill-card:hover{
		box-shadow: 0 0 25px #888e8d, 0 0 25px #888e8d;
	}

	ul.skill-card:hover:after,
	label:hover + ul.skill-card:after,
	input:checked + label + ul.skill-card:after {
		top: -20px;
		transition: var(--t1);
		border-top-color: var(--c1);
	}

	ul.skill-card li {
		--per: 50;
		--dur: calc(calc(var(--per) / 100) * 1.5s);
		margin: 0 0 5px 0;
		list-style: none;
		padding: 20px 0;
		position: relative;
		text-transform: uppercase;
		font-size: 15px;
		color: var(--w2);
	}

	ul.skill-card li:before {
		content: '';
		position: absolute;
		background: #1c1c1c;
		height: 16px;
		width: 100%;
		left: 0;
		bottom: 0;
		border-radius: 2px;
		border: 1px solid #111;
		border-color: #111 #323232 #323232 #111;
		--track: #2292dd40;
		background: linear-gradient(
			90deg,
			var(--track) calc(calc(var(--per) * 1%) + 4px),
			#1c1c1c calc(calc(var(--per) * 1%) + 4px)
		);
	}

	ul.skill-card li:after {
		content: '';
		height: 11px;
		margin: 0 0 2px 0;
		background: var(--c1);
		position: absolute;
		box-shadow: 0px 0px 10px 1px #00c6ff66;
		left: 3px;
		width: 0%;
		bottom: 0;
		transition: all var(--dur) ease 0s;
		animation: start 1s ease 0s 2 alternate;
	}

	ul.skill-card li:hover {
		filter: brightness(1.5);
		transition: var(--t1);
	}

	ul.skill-card:hover li:after,
	label:hover + ul.skill-card li:after,
	input:checked + label + ul.skill-card li:after {
		width: calc(calc(var(--per) * 1%) - 2px);
	}

	@keyframes start {
		100% {
			width: calc(calc(var(--per) * 1%) - 2px);
		}
	}

	ul.skill-card2 li:after {
		animation-delay: 0.5s;
	}
	ul.skill-card3 li:after {
		animation-delay: 1s;
	}

	ul.skill-card li span {
		font-weight: 500;
	}

	ul.skill-card li span:before {
		position: absolute;
		right: -25px;
		top: 43px;
		transition: var(--t1);
		content: '';
		opacity: 1;
		border: 7px solid #fff0;
	}

	ul.skill-card li:hover span:before,
	.profile-skill-card input:checked + label + ul.skill-card li span:before {
		transition: var(--t1);
		right: calc(calc(calc(100 - var(--per)) * 1%) - 12px);
		opacity: 1;
		border-right-color: var(--c1);
	}

	ul.skill-card li span:after {
		position: absolute;
		right: -40px;
		top: 38px;
		transition: var(--t1);
		counter-reset: percent var(--per);
		/*content: counter(percent) "%";*/
		content: counter(percent);
		color: var(--b2);
		opacity: 1 !important;
		padding: 4px 6px;
		border-radius: 1px;
		font-weight: bold;
		pointer-events: none;
	}

	ul.skill-card li:hover span:after,
	.profile-skill-card input:checked + label + ul.skill-card li span:after {
		transition: var(--t1);
		right: calc(calc(85 - var(--per)) * 1%);
		right: calc(calc(calc(100 - var(--per)) * 1%) - 40px);
		opacity: 1;
		background: var(--c1);
	}

	/*********************/
	/*** skill-card VALUES ***/
	/*********************/


	ul.skill-card li.sk-git {
		--per: 90;
	}
	ul.skill-card li.sk-post {
		--per: 90;
	}
	ul.skill-card li.sk-npm {
		--per: 90;
	}

	ul.skill-card li.sk-ang {
		--per: 90;
	}
	ul.skill-card li.sk-svel {
		--per: 90;
	}
	ul.skill-card li.sk-node {
		--per: 90;
	}
	ul.skill-card li.sk-css {
		--per: 90;
	}
	ul.skill-card li.sk-htm {
		--per: 90;
	}

	ul.skill-card li.sk-css {
		--per: 90;
	}
	ul.skill-card li.sk-js {
		--per: 95;
	}

	/*********************/
	/***** TOP LABELS ****/
	/*********************/

	.profile-skill-card input {
		display: none;
	}

	.profile-skill-card label {
		background: var(--w1);
		position: absolute;
		top: -61px;
		left: 22px;
		z-index: 2;
		width: 55px;
		height: 55px;
		border-radius: 100%;
		cursor: pointer;
		transition: var(--t1);
		box-shadow: 0 0 0 0 var(--w1);
	}

	.profile-skill-card label:before {
		content: '';
		position: absolute;
		top: 12px;
		left: 11px;
		z-index: 2;
		width: 33px;
		height: 33px;
		background: transparent;
		transition: var(--t1);
	}

	.profile-skill-card label:hover {
		box-shadow: 0 0 0 3px var(--w1);
		transition: var(--t1);
	}

	.profile-skill-card label:hover:before {
		border-color: var(--b2);
		transition: var(--t1);
	}

	.profile-skill-card input:checked + label {
		/* box-shadow: 0 0 0 6px var(--w1); */
		transition: var(--t1);
	}

	.profile-skill-card input:checked + label:before {
		border-color: var(--c1);
	}

	.profile-skill-card label:before::before {
		content: '';
		position: absolute;
		width: 15px;
		height: 4px;
		background: #000;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
	}

	.profile-skill-card label:before::after {
		content: '';
		position: absolute;
		width: 4px;
		height: 4px;
		background: #000;
		top: 55%;
		left: 40%;
		transform: translate(-50%, -50%);
	}

	.profile-skill-card label:before::after {
		content: '';
		position: absolute;
		width: 4px;
		height: 4px;
		background: #000;
		top: 55%;
		left: 60%;
		transform: translate(-50%, -50%);
	}

	label[for='sk1'] {
		/*left: -10px;*/
	}
	label[for='sk2'] {
		/*left: calc(34% - 6px);*/
	}

	label[for='sk1']:before {
		border-color: cornflowerblue;
	}
	label[for='sk2']:before {
		border-color: cornflowerblue;
	}
	label[for='sk3']:before {
		border-color: cornflowerblue;
	}

	/*********************/
	/*** BOTTOM LABELS ***/
	/*********************/

	ul.skill-card li.more {
		padding: 0;
		margin-bottom: 20px;
	}

	ul.skill-card li.more:before,
	ul.skill-card li.more:after {
		display: none;
	}

	ul.skill-card li.more:hover {
		filter: none !important;
	}

	ul.skill-card li.more div {
		max-height: 0;
		transition: var(--t1);
		overflow: hidden;
		padding: 0;
		width: 100%;
	}
	ul.skill-card li.more input:checked ~ div {
		max-height: 150px;
		transition: var(--t1);
		padding: 20px 0 0;
	}

	ul.skill-card li.more div span:before,
	ul.skill-card li.more div span:after {
		display: none;
	}

	ul.skill-card li.more label {
		background: linear-gradient(163deg, var(--b2) 50%, var(--w1) 50%);
		right: 0;
		left: inherit;
		top: inherit;
		bottom: -70px;
		color: var(--b2);
		background-size: 100% 300%;
		background-position-y: 100%;
		transition: var(--t1);
		width: 55px;
		height: 55px;
		right: -50px;
	}

	ul.skill-card li.more label:before {
		border: 0;
		height: 100%;
		width: 100%;
		transform: rotate(0deg);
		content: '+';
		content: '\271A';
		font-size: 45px;
		line-height: 55px;
		left: 0;
		top: 0;
		text-align: center;
		color: var(--c1);
	}

	ul.skill-card li.more label:hover {
		background-position-y: 0%;
		color: var(--w1) !important;
		transition: var(--t1);
		box-shadow: 0 0 0 10px var(--w1);
	}

	ul.skill-card li.more span {
		background: #1c1c1c;
		border-radius: 1px;
		margin: 10px 10px 1px 1px;
		padding: 4px 8px;
		display: inline-block;
		border: 1px solid #111;
		border-color: #111 #323232 #323232 #111;
	}

	ul.skill-card li.more span:hover {
		color: var(--w0);
		background: var(--c1);
		box-shadow: 0px 0px 5px 1px var(--c1);
		border-color: #fff2;
	}

	ul.skill-card li.more input:checked + label {
		box-shadow: 0 0 0 9px var(--w1);
		background-position-y: 0%;
		color: var(--w0);
		bottom: -70px;
	}

	ul.skill-card li.more input:checked + label:before {
		content: '\2759';
		transform: rotate(90deg);
		font-weight: 600;
	}

	ul.skill-card li.more input:checked + label:hover {
		box-shadow: 0 0 0 0 var(--w1);
		background-position-y: 100%;
		color: var(--b2) !important;
	}

	/*********************/
	/*** MEDIA QUERIES ***/
	/*********************/

	@media only screen and (max-width: 1024px) {
		.content {
			height: 60vh;
		}
		.profile-skill-card {
			flex-direction: row;
			flex-wrap: wrap;
			top: 20px;
		}
		.profile-skill-card > div {
			width: 47% !important;
		}
		.profile-skill-card > div:nth-child(3) {
			width: 98% !important;
			margin-top: 120px;
		}
	}

	/*** Mobile view disabled to get (almost) the desired thumbnail ***/
	/*** Uncomment below code to add the media query for mobile view ***/

	@media only screen and (max-width: 768px) {
		/* .content {
			height: 60vh;
		} */
		.profile-skill-card {
			flex-direction: row;
			flex-wrap: wrap;
			top: 20px;
		}
		.profile-skill-card > div {
			width: 98% !important;
		}
		.profile-skill-card > div:nth-child(2),
		.profile-skill-card > div:nth-child(3) {
			margin-top: 120px;
		}
		ul.skill-card li:after {
			width: calc(calc(var(--per) * 1%) - 2px);
		}
		ul.skill-card li span:before {
			transition: var(--t1);
			right: calc(calc(96.5 - var(--per)) * 1%);
			opacity: 1;
			border-right-color: var(--c1);
		}
		ul.skill-card li span:after {
			transition: var(--t1);
			right: calc(calc(calc(100 - var(--per)) * 1%) - 40px);
			opacity: 1;
			background: var(--c1);
		}
	}
</style>
