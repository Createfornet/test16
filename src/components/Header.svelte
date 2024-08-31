<script>
  import Menu from "./Menu.svelte";

  let isMenuOpen = false
</script>

<header>
  <nav class="flex justify-between">
    <button on:click={() => {isMenuOpen = !isMenuOpen}} class='border px-2'>...</button>
    <span class="text-red-600">zoomit</span>
    <div>profile</div>
  </nav>

  {#if isMenuOpen}
    <Menu/>
  {/if}
</header>