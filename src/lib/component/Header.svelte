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
</script>


<svelte:window bind:scrollY={y} />

<div class="header z-50 {headerPosition == 'unpin' ? 'hidden' : ''}">
	<div class="bg-black text-gray-white p-4">
		<div class="container mx-auto flex justify-between lg:justify-center items-center">
			<nav class="hidden md:flex space-x-4 text-lg font-bold leading-10">
				<a href="#home" class=" hover:text-sky-800 transition">Home</a>
				<a href="#about" class=" hover:text-sky-800 transition">About</a>
				<a href="#services" class=" hover:text-sky-800 transition">Services</a>
				<a href="#skills" class=" hover:text-sky-800 transition">Skills</a>
				<a href="#projects" class=" hover:text-sky-800 transition">Project</a>
				<a href="#contact" class=" hover:text-sky-800 transition">Contact</a>
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
			<li><a href="#home" class="block py-2  hover:text-sky-800 transition">Home</a></li>
			<li><a href="#about" class="block py-2 hover:text-sky-800 transition">About</a></li>
			<li><a href="#services" class="block py-2 hover:text-sky-800 transition">Services</a></li>
			<li><a href="#projects" class="block py-2 hover:text-sky-800 transition">Project</a></li>
			<li><a href="#contact" class="block py-2 hover:text-sky-800 transition">Contact</a></li>
		</ul>
	</div>
</div>




<style>
.text-gray-white{
	color: #CCCCCC;
}

.header{
  position: fixed;
  top: 0;
  transition: top 0.2s ease-in-out;
  width: 100%;
}

</style>