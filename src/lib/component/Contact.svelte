<script>
	import contactUSIMG from '$lib/images/bird_with_letter_transparent.gif';
	let status = '';
	let isContactFormSubmitted = false;
	let isLoading = false;
	const handleSubmit = async (data) => {
		status = 'Submitting...';
		isLoading = true;
		const formData = new FormData(data.currentTarget);
		const object = Object.fromEntries(formData);
		const json = JSON.stringify(object);
		const response = await fetch('https://api.web3forms.com/submit', {
			method: 'POST',
			headers: {
				'Content-Type': 'application/json',
				Accept: 'application/json'
			},
			body: json
		});
		const result = await response.json();
		if (result.success) {
			status = result.message || 'Success';
			isContactFormSubmitted = true;
			isLoading = false;
		} else {
			isLoading = false;
		}
	};
</script>

<section class="contact" id="contact">
	<div class="max-width">
		<h2 class="title">Contact</h2>
		<div class="contact-content">
			<div class="column left">
				<!-- <div class="text">Get in Touch</div>
				<p>
					Feel free to get in touch with me. I'll be happy to answer your questions and set up a
					meeting with you. Reach out and let's create something amazing together!
				</p> -->
				<img src={contactUSIMG} alt="Girl" />
			</div>

			<!-- Reach -->
			<div class="column right">
				{#if !isContactFormSubmitted && !isLoading}
					<div class="text">Message me</div>
					<form on:submit|preventDefault={handleSubmit}>
						<div class="fields">
							<div class="field hidden">
								<input
									type="hidden"
									name="access_key"
									value="74d037ea-59bb-4766-80a2-1fda92e1cb69"
								/>
								<input type="hidden" name="subject" value="portfolio contact us request" />
							</div>
							<div class="field name">
								<input
									class="border border-transparent focus:outline-none focus:ring-2 focus:ring-sky-900 focus:border-transparent"
									type="text"
									autocomplete="off"
									name="name"
									placeholder="Your Name"
									required
								/>
							</div>
							<div class="field email">
								<input
									class="border border-transparent focus:outline-none focus:ring-2 focus:ring-sky-900 focus:border-transparent"
									type="email"
									autocomplete="off"
									name="email"
									placeholder="Your Email"
									required
								/>
							</div>
						</div>
						<div class="field textarea">
							<textarea
								class="border border-transparent focus:outline-none focus:ring-2 focus:ring-sky-900 focus:border-transparent"
								cols="30"
								autocomplete="off"
								rows="10"
								name="message"
								placeholder="Message.."
								required
							/>
						</div>
						<div class="button-area">
							<button type="submit">Submit</button>
						</div>

						
					</form>
				{:else if isLoading}
					<div class="flex justify-center items-center">
						<div aria-label="Loading..." role="status" class="flex items-center space-x-2">
							<svg class="h-20 w-20 animate-spin stroke-sky-900" viewBox="0 0 256 256">
								<line
									x1="128"
									y1="32"
									x2="128"
									y2="64"
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="24"
								/>
								<line
									x1="195.9"
									y1="60.1"
									x2="173.3"
									y2="82.7"
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="24"
								/>
								<line
									x1="224"
									y1="128"
									x2="192"
									y2="128"
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="24"
								/>
								<line
									x1="195.9"
									y1="195.9"
									x2="173.3"
									y2="173.3"
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="24"
								/>
								<line
									x1="128"
									y1="224"
									x2="128"
									y2="192"
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="24"
								/>
								<line
									x1="60.1"
									y1="195.9"
									x2="82.7"
									y2="173.3"
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="24"
								/>
								<line
									x1="32"
									y1="128"
									x2="64"
									y2="128"
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="24"
								/>
								<line
									x1="60.1"
									y1="60.1"
									x2="82.7"
									y2="82.7"
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="24"
								/>
							</svg>
							<span class="text-4xl font-medium text-sky-900">Loading...</span>
						</div>
					</div>
				{:else}
					<svg viewBox="0 0 24 24" class="text-sky-900 w-16 h-16 mx-auto my-6">
						<path
							fill="currentColor"
							d="M12,0A12,12,0,1,0,24,12,12.014,12.014,0,0,0,12,0Zm6.927,8.2-6.845,9.289a1.011,1.011,0,0,1-1.43.188L5.764,13.769a1,1,0,1,1,1.25-1.562l4.076,3.261,6.227-8.451A1,1,0,1,1,18.927,8.2Z"
						/>
					</svg>
					<div
						id="alert-border-1"
						class="flex items-center p-4 mb-4 text-sky-800 border-4 border-blue-300 bg-blue-50 dark:text-blue-400 dark:bg-gray-800 dark:border-sky-800"
						role="alert"
					>
						<div class="ml-3 text-sm font-bold">
							Your message has been sent successfully! I'll contact you shortly.
						</div>
						<button
							type="button"
							class="ml-auto -mx-1.5 -my-1.5 bg-blue-50 text-sky-800 rounded-lg focus:ring-2 focus:ring-blue-400 p-1.5 hover:bg-blue-200 inline-flex items-center justify-center h-8 w-8 dark:bg-gray-800 dark:text-blue-400 dark:hover:bg-gray-700"
							data-dismiss-target="#alert-border-1"
							aria-label="Close"
							on:click={() => (isContactFormSubmitted = false)}
						>
							<span class="sr-only">Dismiss</span>
							<svg
								class="w-3 h-3"
								aria-hidden="true"
								xmlns="http://www.w3.org/2000/svg"
								fill="none"
								viewBox="0 0 14 14"
							>
								<path
									stroke="currentColor"
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="2"
									d="m1 1 6 6m0 0 6 6M7 7l6-6M7 7l-6 6"
								/>
							</svg>
						</button>
					</div>
				{/if}
			</div>
		</div>
	</div>

	<div class="flex flex-wrap justify-center gap-3 mt-20">
							
		_
		<button class="bg-sky-900 p-2 font-semibold text-white inline-flex items-center space-x-2 rounded-full
		hover:scale-105">
		  <svg class="w-5 h-5 fill-current" role="img" viewBox="0 0 256 256" xmlns="http://www.w3.org/2000/svg">
			<g><path d="M218.123122,218.127392 L180.191928,218.127392 L180.191928,158.724263 C180.191928,144.559023 179.939053,126.323993 160.463756,126.323993 C140.707926,126.323993 137.685284,141.757585 137.685284,157.692986 L137.685284,218.123441 L99.7540894,218.123441 L99.7540894,95.9665207 L136.168036,95.9665207 L136.168036,112.660562 L136.677736,112.660562 C144.102746,99.9650027 157.908637,92.3824528 172.605689,92.9280076 C211.050535,92.9280076 218.138927,118.216023 218.138927,151.114151 L218.123122,218.127392 Z M56.9550587,79.2685282 C44.7981969,79.2707099 34.9413443,69.4171797 34.9391618,57.260052 C34.93698,45.1029244 44.7902948,35.2458562 56.9471566,35.2436736 C69.1040185,35.2414916 78.9608713,45.0950217 78.963054,57.2521493 C78.9641017,63.090208 76.6459976,68.6895714 72.5186979,72.8184433 C68.3913982,76.9473153 62.7929898,79.26748 56.9550587,79.2685282 M75.9206558,218.127392 L37.94995,218.127392 L37.94995,95.9665207 L75.9206558,95.9665207 L75.9206558,218.127392 Z M237.033403,0.0182577091 L18.8895249,0.0182577091 C8.57959469,-0.0980923971 0.124827038,8.16056231 -0.001,18.4706066 L-0.001,237.524091 C0.120519052,247.839103 8.57460631,256.105934 18.8895249,255.9977 L237.033403,255.9977 C247.368728,256.125818 255.855922,247.859464 255.999,237.524091 L255.999,18.4548016 C255.851624,8.12438979 247.363742,-0.133792868 237.033403,0.000790807055"></path></g>
		  </svg>
		</button>

		
		<button class="bg-sky-900 p-2 font-semibold text-white inline-flex items-center space-x-2 rounded-full hover:scale-105">
		  <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" role="img" class="w-5" preserveAspectRatio="xMidYMid meet" viewBox="0 0 24 24">
			<g fill="none"><path fill-rule="evenodd" clip-rule="evenodd" d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385c.6.105.825-.255.825-.57c0-.285-.015-1.23-.015-2.235c-3.015.555-3.795-.735-4.035-1.41c-.135-.345-.72-1.41-1.23-1.695c-.42-.225-1.02-.78-.015-.795c.945-.015 1.62.87 1.845 1.23c1.08 1.815 2.805 1.305 3.495.99c.105-.78.42-1.305.765-1.605c-2.67-.3-5.46-1.335-5.46-5.925c0-1.305.465-2.385 1.23-3.225c-.12-.3-.54-1.53.12-3.18c0 0 1.005-.315 3.3 1.23c.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23c.66 1.65.24 2.88.12 3.18c.765.84 1.23 1.905 1.23 3.225c0 4.605-2.805 5.625-5.475 5.925c.435.375.81 1.095.81 2.22c0 1.605-.015 2.895-.015 3.3c0 .315.225.69.825.57A12.02 12.02 0 0 0 24 12c0-6.63-5.37-12-12-12z" fill="currentColor" /></g>
		  </svg>
		</button>
		_
	  </div>
</section>

<style>
	.contact {
		padding: 100px 0;
	}

	.title {
		margin-bottom: 0px !important;
	}
</style>