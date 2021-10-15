<script lang="ts">
  let isOpen: Boolean = false;

  function toggleIsOpen(): void {
    isOpen = !isOpen;
    console.log('flipping that burg', isOpen);
  }

  function animateInOrOut(): void {
    console.log('transition');
  }

  function handleBurgerClick (): void {
    toggleIsOpen();
  }
</script>

{#if !isOpen}
<div class="hamburger" on:click={handleBurgerClick}>
  <svg viewBox="0 0 100 80" width="44" height="44">
    <rect width="100" height="14"></rect>
    <rect y="30" width="100" height="14"></rect>
    <rect y="60" width="100" height="14"></rect>
  </svg>
</div>
{/if}

{#if isOpen}
<div class="hamburger" on:click={handleBurgerClick}>
  <svg viewBox="0 0 100 80" width="44" height="44">
    <rect width="100" height="14"></rect>
    <rect y="30" width="100" height="14"></rect>
    <rect y="60" width="100" height="14"></rect>
  </svg>
</div>
{/if}

<style>
  .hamburger {
    margin: 0;
    display: flex;
    justify-content: center;
  }
</style>