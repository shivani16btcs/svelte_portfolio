<script>
    let isMobileMenuOpen = false;
  
    function toggleMobileMenu() {
        isMobileMenuOpen = !isMobileMenuOpen;
    }
</script>

<div class="bg-black text-green-500 p-4">
    <div class="container mx-auto flex justify-between lg:justify-center items-center">
        <nav class="hidden md:flex space-x-4 text-lg font-bold leading-10">
            <a href="#home" class="text-white hover:text-green-500 transition">Home</a>
            <a href="#about" class="text-white hover:text-green-500 transition">About</a>
            <a href="#services" class="text-white hover:text-green-500 transition">Services</a>
            <a href="#projects" class="text-white hover:text-green-500 transition">Project</a>
            <a href="#contact" class="text-white hover:text-green-500 transition">Contact</a>
        </nav>
        <div class="md:hidden">
            <button on:click={toggleMobileMenu} class="text-white text-2xl ml-4 transform transition-transform" style="transform: {isMobileMenuOpen ? 'rotate(90deg)' : 'rotate(0)'}">&#9776;</button>
        </div>
    </div>
</div>
<div class="bg-black text-green-500 text-center transition-all transform origin-top" style="max-height: {isMobileMenuOpen ? '1000px' : '0'}; overflow: hidden; transition: max-height 0.5s ease-in-out;">
    <ul class="py-4">
        <li><a href="#home" class="block py-2 hover:text-green-500 transition">Home</a></li>
        <li><a href="#about" class="block py-2 hover:text-green-500 transition">About</a></li>
        <li><a href="#services" class="block py-2 hover:text-green-500 transition">Services</a></li>
        <li><a href="#projects" class="block py-2 hover:text-green-500 transition">Project</a></li>
        <li><a href="#contact" class="block py-2 hover:text-green-500 transition">Contact</a></li>
    </ul>
</div>