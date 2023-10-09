<script>
	let isMobileMenuOpen = false;
	let headerPosition = 'pin';
	let y = 0;
	let lastY = 0;

	function toggleMobileMenu() {
		isMobileMenuOpen = !isMobileMenuOpen;
	}

	//pin header on up scroll and unpin on down scroll
	function findHeaderPosition(y = 0, scrolled = 0) {
		if (y < 0) return 'pin';
		if (!scrolled || Math.abs(scrolled) < 0) return headerPosition;
		const dir = scrolled < 0 ? 'down' : 'up';
		if (dir === 'up') return 'pin';
		//find if scroll height is more then header height
		if (dir === 'down' && y > 40) {
			return 'unpin';
		}
		return headerPosition;
	}

	function checkHeaderPosition(y = 0) {
		const scrolledPxs = lastY - y;
		const result = findHeaderPosition(y, scrolledPxs);
		lastY = y;
		return result;
	}
	$: headerPosition = checkHeaderPosition(y);

	// Add an array to store the section IDs
	const sectionIds = ['home', 'about', 'services', 'skills', 'projects', 'contact'];
	let activeSection = sectionIds[0]; // Initialize with the first section

	// Function to determine the active section based on scroll position
	function setActiveSection() {
		for (const id of sectionIds) {
			const section = document.getElementById(id);
			if (section) {
				const rect = section.getBoundingClientRect();
				if (rect.top <= 100 && rect.bottom >= 100) {
					activeSection = id;
					console.log("activeSection",activeSection)
					break;
				}
			}
		}
	}

	// Call setActiveSection on scroll
	function handleScroll() {
		setActiveSection();
	}

	// Add a scroll event listener to the window
	window.addEventListener('scroll', handleScroll);
</script>

<svelte:window bind:scrollY={y} />

<div class="header z-50 {headerPosition == 'unpin' ? 'hidden' : ''}">
	<div class="text-gray-white p-4">
		<div class="container mx-auto flex justify-between lg:justify-center items-center">
			<nav class="hidden md:flex space-x-8 text-lg font-semibold leading-10">
				<a href="#home" class=" hover:text-sky-800 transition {activeSection==sectionIds[0]?'active':''}" >Home</a>
				<a href="#about" class=" hover:text-sky-800 transition {activeSection==sectionIds[1]?'active':''}">About</a>
				<a href="#services" class=" hover:text-sky-800 transition {activeSection==sectionIds[2]?'active':''}">Services</a>
				<a href="#skills" class=" hover:text-sky-800 transition {activeSection==sectionIds[3]?'active':''}">Skills</a>
				<a href="#projects" class=" hover:text-sky-800 transition {activeSection==sectionIds[4]?'active':''}">Project</a>
				<a href="#contact" class=" hover:text-sky-800 transition {activeSection==sectionIds[5]?'active':''}">Contact</a>
			</nav>
			<div class="md:hidden">
				<button
					on:click={toggleMobileMenu}
					class="text-gray-white text-2xl ml-4 transform transition-transform"
					style="transform: {isMobileMenuOpen ? 'rotate(90deg)' : 'rotate(0)'}">&#9776;</button
				>
			</div>
		</div>
	</div>
	<div
		class="bg-black text-gray-white text-center transition-all transform origin-top"
		style="max-height: {isMobileMenuOpen
			? '1000px'
			: '0'}; overflow: hidden; transition: max-height 0.5s ease-in-out;"
	>
		<ul class="py-4">
			<li><a href="#home" class="block py-2 hover:text-sky-800 transition {activeSection==sectionIds[0]?'active':''}">Home</a></li>
			<li><a href="#about" class="block py-2 hover:text-sky-800 transition {activeSection==sectionIds[1]?'active':''}">About</a></li>
			<li><a href="#services" class="block py-2 hover:text-sky-800 transition {activeSection==sectionIds[2]?'active':''}">Services</a></li>
			<li><a href="#skills" class="block py-2 hover:text-sky-800 transition {activeSection==sectionIds[3]?'active':''}">Skills</a></li>
			<li><a href="#projects" class="block py-2 hover:text-sky-800 transition {activeSection==sectionIds[4]?'active':''}">Project</a></li>
			<li><a href="#contact" class="block py-2 hover:text-sky-800 transition {activeSection==sectionIds[5]?'active':''}">Contact</a></li>
		</ul>
	</div>
</div>

<style>
	.text-gray-white {
		color: #cccccc;
	}

	.header {
		position: fixed;
		top: 0;
		transition: top 0.2s ease-in-out;
		width: 100%;
		background: #0a0a0a;
	}

.active{
	--tw-text-opacity: 1;
    color: rgb(7 89 133 / var(--tw-text-opacity));
	text-decoration: underline;
}
</style>
