<script>
  import Logo from './Logo.svelte';
  import Hamburger from './Hamburger.svelte';
</script>

<header>
  <Logo />
  Purposeful Agency
  <Hamburger />
</header>

<style>
  header {
    display: flex;
    padding: 16px;
    justify-content: space-between;
    font-size: 2em;
    align-items: center;
    background-color: #db5cdb;
  }
</style>