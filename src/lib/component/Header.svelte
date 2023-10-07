<script>
	let isMobileMenuOpen = false;

	function toggleMobileMenu() {
		isMobileMenuOpen = !isMobileMenuOpen;
	}
</script>

<div class="bg-black text-gray-white p-4">
	<div class="container mx-auto flex justify-between lg:justify-center items-center">
		<nav class="hidden md:flex space-x-4 text-lg font-bold leading-10">
			<a href="#home" class=" hover:text-sky-900 transition">Home</a>
			<a href="#about" class=" hover:text-sky-900 transition">About</a>
			<a href="#services" class=" hover:text-sky-900 transition">Services</a>
			<a href="#skills" class=" hover:text-sky-900 transition">Skills</a>
			<a href="#projects" class=" hover:text-sky-900 transition">Project</a>
			<a href="#contact" class=" hover:text-sky-900 transition">Contact</a>
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
		<li><a href="#home" class="block py-2  hover:text-sky-900 transition">Home</a></li>
		<li><a href="#about" class="block py-2 hover:text-sky-900 transition">About</a></li>
		<li><a href="#services" class="block py-2 hover:text-sky-900 transition">Services</a></li>
		<li><a href="#projects" class="block py-2 hover:text-sky-900 transition">Project</a></li>
		<li><a href="#contact" class="block py-2 hover:text-sky-900 transition">Contact</a></li>
	</ul>
</div>



<style>
.text-gray-white{
	color: #CCCCCC;
	/* font-family: 'Courier New', monospace; */

}
</style>