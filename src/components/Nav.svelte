<!-- NAV BAR -->
<script>
  let isOpen = false;

  const handleMenuState = () => {
    return (isOpen = !isOpen);
  };
</script>

<header class="sticky">
  <nav class="flex justify-between items-center  bg-gray-100 shadow mb-8">
    <div class="flex items-center p-3">
      <img class="w-10" src="cat.png" alt="Cat Logo" />
      <a class="text-2xl font-bold" href="#"
        ><span class="text-keyRed">Meow</span>Latte.</a
      >
    </div>
    <div class="md:flex md:space-x-6 md:mx-8 hidden">
      <a class="text-lg text-keyRed hover:underline" href="#">Menu</a>
      <a class="text-lg text-keyRed hover:underline" href="#">About</a>
      <a class="text-lg text-keyRed hover:underline" href="#">Contact</a>
    </div>
    <div class="flex mx-8 md:hidden">
      <button
        on:click={handleMenuState}
        type="button"
        class="text-gray hover:text-keyRed transition duration-100 ease-in-out focus:outline-none"
      >
        <svg class="h-10 w-10 fill-current" viewBox="0 0 24 24">
          {#if !isOpen}
            <path
              fill-rule="evenodd"
              d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z"
            />
          {:else if isOpen}
            <path
              fill-rule="evenodd"
              d="M18.278 16.864a1 1 0 0 1-1.414 1.414l-4.829-4.828-4.828 4.828a1 1 0 0 1-1.414-1.414l4.828-4.829-4.828-4.828a1 1 0 0 1 1.414-1.414l4.829 4.828 4.828-4.828a1 1 0 1 1 1.414 1.414l-4.828 4.829 4.828 4.828z"
            />
          {/if}
        </svg>
      </button>
    </div>
  </nav>
</header>
