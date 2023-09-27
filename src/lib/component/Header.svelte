<script>
	let isMobileMenuOpen = false;
  
	function toggleMobileMenu() {
	  isMobileMenuOpen = !isMobileMenuOpen;
	}
  </script>
  
  <div class="bg-blue-500 p-4">
	<div class="container mx-auto flex justify-between lg:justify-center items-center">
	  <nav class="hidden md:flex space-x-4">
		<a href="#" class="text-white hover:text-blue-300 transition">Home</a>
		<a href="#" class="text-white hover:text-blue-300 transition">About</a>
		<a href="#" class="text-white hover:text-blue-300 transition">Portfolio</a>
		<a href="#" class="text-white hover:text-blue-300 transition">Contact</a>
	  </nav>
	  <div class="md:hidden">
		<button on:click={toggleMobileMenu} class="text-white text-2xl ml-4 transform transition-transform" style="transform: {isMobileMenuOpen ? 'rotate(90deg)' : 'rotate(0)'}">&#9776;</button>
	  </div>
	</div>
  </div>
  <div class="bg-blue-500 text-white text-center transition-all transform origin-top" style="max-height: {isMobileMenuOpen ? '1000px' : '0'}; overflow: hidden; transition: max-height 0.5s ease-in-out;">
	<ul class="py-4">
	  <li><a href="#" class="block py-2 hover:bg-blue-400 transition">Home</a></li>
	  <li><a href="#" class="block py-2 hover:bg-blue-400 transition">About</a></li>
	  <li><a href="#" class="block py-2 hover:bg-blue-400 transition">Portfolio</a></li>
	  <li><a href="#" class="block py-2 hover:bg-blue-400 transition">Contact</a></li>
	</ul>
  </div>