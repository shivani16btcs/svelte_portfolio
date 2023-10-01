<div class="content flex justify-center items-center">
	<div class="profile-skills">
		<div>
			<!-- <span id="sk1"></span> -->
			<label
				for="sk1"
				class="flex justify-center items-center transform transition-transform hover:scale-125"
			>
				<!-- smile svg  -->
				<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" width="33" height="33">
					<!-- Face -->
					<circle cx="50" cy="50" r="40" stroke="#007BA7" stroke-width="2" fill="transparent" />

					<!-- Left eye -->
					<circle cx="35" cy="40" r="5" fill="#007BA7" />

					<!-- Right eye -->
					<circle cx="65" cy="40" r="5" fill="#007BA7" />

					<!-- Mouth (a simple curve) -->
					<path d="M35 60 Q 50 75 65 60" fill="transparent" stroke="#1e3551" stroke-width="2" />
				</svg>
			</label>
			<ul class="skills skills1">
				<li class="sk-cms"><span>CMS</span></li>
				<li class="sk-dtb"><span>DDBB</span></li>
				<li class="sk-dis"><span>Design</span></li>
				<li class="sk-pro"><span>Programing</span></li>
				<li class="sk-ani"><span>Animation</span></li>
				<li class="more">
					<input type="checkbox" id="more-con" /><label for="more-con" />
					<div>
						<span>PHOTO</span><span>API</span><span>MAPS</span><span>VIDEO</span><span>CHARTS</span
						><span>RWD</span>
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
					<circle cx="50" cy="50" r="40" stroke="#007BA7" stroke-width="2" fill="transparent" />

					<!-- Left eye -->
					<circle cx="35" cy="40" r="5" fill="#007BA7" />

					<!-- Right eye -->
					<circle cx="65" cy="40" r="5" fill="#007BA7" />

					<!-- Mouth (a simple curve) -->
					<path d="M35 60 Q 50 75 65 60" fill="transparent" stroke="#1e3551" stroke-width="2" />
				</svg>
			</label>
			<ul class="skills skills2">
				<li class="sk-gim"><span>Gimp</span></li>
				<li class="sk-ado"><span>Adobe&nbsp;CC</span></li>
				<li class="sk-not"><span>Notepad++</span></li>
				<li class="sk-tri"><span>Tridion</span></li>
				<li class="sk-wor"><span>Wordpress</span></li>
				<li class="more">
					<input type="checkbox" id="more-pro" /><label for="more-pro" />
					<div>
						<span>JOOMLA</span><span>DRUPAL</span><span>JIRA</span><span>TRELLO</span><span
							>FILEZILLA</span
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
					<circle cx="50" cy="50" r="40" stroke="#007BA7" stroke-width="2" fill="transparent" />

					<!-- Left eye -->
					<circle cx="35" cy="40" r="5" fill="#007BA7" />

					<!-- Right eye -->
					<circle cx="65" cy="40" r="5" fill="#007BA7" />

					<!-- Mouth (a simple curve) -->
					<path d="M35 60 Q 50 75 65 60" fill="transparent" stroke="#1e3551" stroke-width="2" />
				</svg>
			</label>
			<ul class="skills skills3">
				<li class="sk-css"><span>CSS</span></li>
				<li class="sk-htm"><span>HTML</span></li>
				<li class="sk-jav"><span>JS</span></li>
				<li class="sk-php"><span>PHP</span></li>
				<li class="sk-sql"><span>SQL</span></li>
				<li class="more">
					<input type="checkbox" id="more-len" /><label for="more-len" />
					<div>
						<span>XHTML</span><span>XSL</span><span>XML</span><span>JSON</span><span>PUG</span><span
							>SASS</span
						>
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
		--c1: #007ba7;
		--b2: #222;
		--b3: #333;
		--w1: #fff;
		--w2: #eee;
		--t1: all 0.5s ease 0s;
	}

	body {
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
	}

	.content {
		width: 80vw;
		background: #fff0;
	}

	.profile-skills {
		display: flex;
		top: 150px;
		position: relative;
		width: 100%;
		align-items: flex-start;
	}

	.profile-skills > div {
		width: 32%;
		margin-right: 3%;
		border-radius: 2px;
		position: relative;
	}

	ul.skills {
		width: 100%;
		position: relative;
		padding: 25px 35px;
		background: linear-gradient(
			0deg,
			var(--c1) 0 10px,
			var(--b2) 0 calc(100% - 10px),
			var(--c1) 0 100%
		);
	}

	ul.skills:before {
		content: 'Skills';
		text-transform: uppercase;
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
		font-size: 30px;
		line-height: 35px;
		transform: scaleY(1.65);
		border-radius: 6px;
	}

	ul.skills2:before {
		content: 'Tools';
	}

	ul.skills3:before {
		content: 'Codes';
	}

	ul.skills:after {
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

	ul.skills:hover:before,
	label:hover + ul.skills:before,
	input:checked + label + ul.skills:before {
		transition: var(--t1);
		background-color: #007ba7;
		background-position: 0 50%;
	}
	ul.skills:hover:after,
	label:hover + ul.skills:after,
	input:checked + label + ul.skills:after {
		top: -20px;
		transition: var(--t1);
		border-top-color: #007ba7;
	}

	ul.skills li {
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

	ul.skills li:before {
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

	ul.skills li:after {
		content: '';
		height: 11px;
		margin: 0 0 2px 0;
		background: #007ba7;
		position: absolute;
		box-shadow: 0px 0px 10px 1px #00c6ff66;
		left: 3px;
		width: 0%;
		bottom: 0;
		transition: all var(--dur) ease 0s;
		animation: start 1s ease 0s 2 alternate;
	}

	ul.skills li:hover {
		filter: brightness(1.5);
		transition: var(--t1);
	}

	ul.skills:hover li:after,
	label:hover + ul.skills li:after,
	input:checked + label + ul.skills li:after {
		width: calc(calc(var(--per) * 1%) - 2px);
	}

	@keyframes start {
		100% {
			width: calc(calc(var(--per) * 1%) - 2px);
		}
	}

	ul.skills2 li:after {
		animation-delay: 0.5s;
	}
	ul.skills3 li:after {
		animation-delay: 1s;
	}

	ul.skills li span {
		font-weight: 500;
	}

	ul.skills li span:before {
		position: absolute;
		right: -25px;
		top: 43px;
		transition: var(--t1);
		content: '';
		opacity: 1;
		border: 7px solid #fff0;
	}

	ul.skills li:hover span:before,
	.profile-skills input:checked + label + ul.skills li span:before {
		transition: var(--t1);
		right: calc(calc(calc(100 - var(--per)) * 1%) - 12px);
		opacity: 1;
		border-right-color: #007ba7;
	}

	ul.skills li span:after {
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

	ul.skills li:hover span:after,
	.profile-skills input:checked + label + ul.skills li span:after {
		transition: var(--t1);
		right: calc(calc(85 - var(--per)) * 1%);
		right: calc(calc(calc(100 - var(--per)) * 1%) - 40px);
		opacity: 1;
		background: var(--c1);
	}

	/*********************/
	/*** SKILLS VALUES ***/
	/*********************/

	ul.skills li.sk-ani {
		--per: 85;
	}
	ul.skills li.sk-cms {
		--per: 75;
	}
	ul.skills li.sk-dis {
		--per: 90;
	}
	ul.skills li.sk-dtb {
		--per: 65;
	}
	ul.skills li.sk-pro {
		--per: 60;
	}
	ul.skills li.sk-res {
		--per: 90;
	}

	ul.skills li.sk-gim {
		--per: 90;
	}
	ul.skills li.sk-ado {
		--per: 60;
	}
	ul.skills li.sk-not {
		--per: 85;
	}
	ul.skills li.sk-tri {
		--per: 70;
	}
	ul.skills li.sk-wor {
		--per: 90;
	}
	ul.skills li.sk-tre {
		--per: 65;
	}

	ul.skills li.sk-css {
		--per: 95;
	}
	ul.skills li.sk-htm {
		--per: 90;
	}
	ul.skills li.sk-jav {
		--per: 70;
	}
	ul.skills li.sk-php {
		--per: 80;
	}
	ul.skills li.sk-sql {
		--per: 65;
	}
	ul.skills li.sk-pug {
		--per: 40;
	}

	/*********************/
	/***** TOP LABELS ****/
	/*********************/

	.profile-skills input {
		display: none;
	}

	.profile-skills label {
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

	.profile-skills label:before {
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

	.profile-skills label:hover {
		box-shadow: 0 0 0 3px var(--w1);
		transition: var(--t1);
	}

	.profile-skills label:hover:before {
		border-color: var(--b2);
		transition: var(--t1);
	}

	.profile-skills input:checked + label {
		box-shadow: 0 0 0 6px var(--w1);
		transition: var(--t1);
	}

	.profile-skills input:checked + label:before {
		border-color: #007ba7;
	}

	.profile-skills label:before::before {
		content: '';
		position: absolute;
		width: 15px;
		height: 4px;
		background: #000;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
	}

	.profile-skills label:before::after {
		content: '';
		position: absolute;
		width: 4px;
		height: 4px;
		background: #000;
		top: 55%;
		left: 40%;
		transform: translate(-50%, -50%);
	}

	.profile-skills label:before::after {
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

	ul.skills li.more {
		padding: 0;
		margin-bottom: 20px;
	}

	ul.skills li.more:before,
	ul.skills li.more:after {
		display: none;
	}

	ul.skills li.more:hover {
		filter: none !important;
	}

	ul.skills li.more div {
		max-height: 0;
		transition: var(--t1);
		overflow: hidden;
		padding: 0;
		width: 100%;
	}
	ul.skills li.more input:checked ~ div {
		max-height: 150px;
		transition: var(--t1);
		padding: 20px 0 0;
	}

	ul.skills li.more div span:before,
	ul.skills li.more div span:after {
		display: none;
	}

	ul.skills li.more label {
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

	ul.skills li.more label:before {
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

	ul.skills li.more label:hover {
		background-position-y: 0%;
		color: var(--w1) !important;
		transition: var(--t1);
		box-shadow: 0 0 0 10px var(--w1);
	}

	ul.skills li.more span {
		background: #1c1c1c;
		border-radius: 1px;
		margin: 10px 10px 1px 1px;
		padding: 4px 8px;
		display: inline-block;
		border: 1px solid #111;
		border-color: #111 #323232 #323232 #111;
	}

	ul.skills li.more span:hover {
		color: var(--w0);
		background: var(--c1);
		box-shadow: 0px 0px 5px 1px var(--c1);
		border-color: #fff2;
	}

	ul.skills li.more input:checked + label {
		box-shadow: 0 0 0 9px var(--w1);
		background-position-y: 0%;
		color: var(--w0);
		bottom: -70px;
	}

	ul.skills li.more input:checked + label:before {
		content: '\2759';
		transform: rotate(90deg);
		font-weight: 600;
	}

	ul.skills li.more input:checked + label:hover {
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
		.profile-skills {
			flex-direction: row;
			flex-wrap: wrap;
			top: 20px;
		}
		.profile-skills > div {
			width: 47% !important;
		}
		.profile-skills > div:nth-child(3) {
			width: 98% !important;
			margin-top: 120px;
		}
	}

	/*** Mobile view disabled to get (almost) the desired thumbnail ***/
	/*** Uncomment below code to add the media query for mobile view ***/

	@media only screen and (max-width: 768px) {
		.content {
			height: 60vh;
		}
		.profile-skills {
			flex-direction: row;
			flex-wrap: wrap;
			top: 20px;
		}
		.profile-skills > div {
			width: 98% !important;
		}
		.profile-skills > div:nth-child(2),
		.profile-skills > div:nth-child(3) {
			margin-top: 120px;
		}
		ul.skills li:after {
			width: calc(calc(var(--per) * 1%) - 2px);
		}
		ul.skills li span:before {
			transition: var(--t1);
			right: calc(calc(96.5 - var(--per)) * 1%);
			opacity: 1;
			border-right-color: #007ba7;
		}
		ul.skills li span:after {
			transition: var(--t1);
			right: calc(calc(calc(100 - var(--per)) * 1%) - 40px);
			opacity: 1;
			background: var(--c1);
		}
	}
</style>
