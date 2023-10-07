<script>
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
		<h2 class="title">Contact Me</h2>
		<div class="contact-content">
			<div class="column left">
				<div class="text">Get in Touch</div>
				<p>
					Feel free to get in touch with me. I'll be happy to answer your questions and set up a
					meeting with you. Reach out and let's create something amazing together!
				</p>
				<!-- <div class="info mt-1">
					<div class="font-semibold">Language Known</div>
					<div class="sub-title">Hindi, English</div>
				</div> -->
				<div class="mt-2">
					<!-- Social -->
					<a href="https://www.linkedin.com/in/shivani-yadav-abc/" class="mr-2 contact-social-icon">
						<button
							type="button"
							data-te-ripple-init
							data-te-ripple-color="light"
							class="hover:animate-bounce   mb-2 inline-block rounded-full px-3 py-2.5 text-xs font-medium uppercase leading-normal text-white shadow-md transition duration-150 ease-in-out hover:shadow-lg focus:shadow-lg focus:outline-none focus:ring-0 active:shadow-lg"
							style="background-color: #1e3551"
						>
							<svg
								xmlns="http://www.w3.org/2000/svg"
								class="h-3 w-3"
								fill="currentColor"
								viewBox="0 0 24 24"
							>
								<path
									d="M4.98 3.5c0 1.381-1.11 2.5-2.48 2.5s-2.48-1.119-2.48-2.5c0-1.38 1.11-2.5 2.48-2.5s2.48 1.12 2.48 2.5zm.02 4.5h-5v16h5v-16zm7.982 0h-4.968v16h4.969v-8.399c0-4.67 6.029-5.052 6.029 0v8.399h4.988v-10.131c0-7.88-8.922-7.593-11.018-3.714v-2.155z"
								/>
							</svg>
						</button>
					</a>

					<a href="https://github.com/shivani16btcs"  class="contact-social-icon">
						<button
							type="button"
							data-te-ripple-init
							data-te-ripple-color="light"
							class="hover:animate-bounce mb-2 inline-block rounded-full px-3 py-2.5 text-xs font-medium uppercase leading-normal text-white shadow-md transition duration-150 ease-in-out hover:shadow-lg focus:shadow-lg focus:outline-none focus:ring-0 active:shadow-lg"
							style="background-color: #1e3551"
						>
							<svg
								xmlns="http://www.w3.org/2000/svg"
								class="h-3 w-3"
								fill="currentColor"
								viewBox="0 0 24 24"
							>
								<path
									d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"
								/>
							</svg>
						</button>
					</a>
				</div>
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
							</div>
							<div class="field name">
								<input type="text" name="name" placeholder="Your Name" required />
							</div>
							<div class="field email">
								<input type="email" name="email" placeholder="Your Email" required />
							</div>
						</div>
						<div class="field">
							<input type="text" name="subject" placeholder="Subject" required />
						</div>
						<div class="field textarea">
							<textarea cols="30" rows="10" name="message" placeholder="Message.." required />
						</div>
						<div class="button-area">
							<button type="submit">Send message</button>
						</div>
					</form>
				{:else if isLoading}
					<div class="flex justify-center items-center">
						<!-- <div
							class="h-8 w-8 animate-spin rounded-full border-4 border-solid border-current border-r-transparent align-[-0.125em] text-sky-900 motion-reduce:animate-[spin_1.5s_linear_infinite]"
							role="status"
						>
							<span
								class="!absolute !-m-px !h-px !w-px !overflow-hidden !whitespace-nowrap !border-0 !p-0 ![clip:rect(0,0,0,0)]"
								>Loading...</span
							>
						</div> -->
						<div aria-label="Loading..." role="status" class="flex items-center space-x-2">
							<svg class="h-20 w-20 animate-spin stroke-sky-900" viewBox="0 0 256 256">
								<line x1="128" y1="32" x2="128" y2="64" stroke-linecap="round" stroke-linejoin="round" stroke-width="24"></line>
								<line x1="195.9" y1="60.1" x2="173.3" y2="82.7" stroke-linecap="round" stroke-linejoin="round"
									stroke-width="24"></line>
								<line x1="224" y1="128" x2="192" y2="128" stroke-linecap="round" stroke-linejoin="round" stroke-width="24">
								</line>
								<line x1="195.9" y1="195.9" x2="173.3" y2="173.3" stroke-linecap="round" stroke-linejoin="round"
									stroke-width="24"></line>
								<line x1="128" y1="224" x2="128" y2="192" stroke-linecap="round" stroke-linejoin="round" stroke-width="24">
								</line>
								<line x1="60.1" y1="195.9" x2="82.7" y2="173.3" stroke-linecap="round" stroke-linejoin="round"
									stroke-width="24"></line>
								<line x1="32" y1="128" x2="64" y2="128" stroke-linecap="round" stroke-linejoin="round" stroke-width="24"></line>
								<line x1="60.1" y1="60.1" x2="82.7" y2="82.7" stroke-linecap="round" stroke-linejoin="round" stroke-width="24">
								</line>
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
</section>

<style>
	.contact {
		padding: 100px 0;
	}

	
</style>
