<script lang="ts">
  let isMenuOpen: boolean = false;

  function toggleMenu(): void {
    isMenuOpen = !isMenuOpen;
  }
</script>

<nav class="bg-gray-800 p-4">
  <div class="container mx-auto flex justify-between items-center">
    <div class="text-white text-lg font-semibold">
      MyWebsite
    </div>
    <div class="hidden md:flex space-x-4">
      <a href="#" class="text-gray-300 hover:text-white">Home</a>
      <a href="#" class="text-gray-300 hover:text-white">About</a>
      <a href="#" class="text-gray-300 hover:text-white">Services</a>
      <a href="#" class="text-gray-300 hover:text-white">Contact</a>
    </div>
    <div class="md:hidden">
      <button on:click={toggleMenu} class="text-white focus:outline-none">
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path>
        </svg>
      </button>
    </div>
  </div>

  <!-- Mobile Menu -->
  <div class={isMenuOpen ? 'block' : 'hidden'} md:hidden>
    <a href="#" class="block text-gray-300 hover:text-white px-4 py-2">Home</a>
    <a href="#" class="block text-gray-300 hover:text-white px-4 py-2">About</a>
    <a href="#" class="block text-gray-300 hover:text-white px-4 py-2">Services</a>
    <a href="#" class="block text-gray-300 hover:text-white px-4 py-2">Contact</a>
  </div>
</nav>
