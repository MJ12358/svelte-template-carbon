<script>
  import {
    Content,
    Header,
    ImageLoader,
    Link,
    SideNav,
    SideNavItems,
    SideNavLink,
  } from 'carbon-components-svelte';
  import Counter from './presentation/Counter.svelte';
  import svelteLogo from '/assets/logos/svelte.svg';
  import viteLogo from '/assets/logos/vite.svg';

  let isSideNavOpen = false;
</script>

<Header company="IBM" platformName="Carbon Svelte" bind:isSideNavOpen />

<SideNav bind:isOpen={isSideNavOpen}>
  <SideNavItems>
    <SideNavLink text="Link 1" />
    <SideNavLink text="Link 2" />
    <SideNavLink text="Link 3" />
  </SideNavItems>
</SideNav>

<Content>
  <div>
    <Link href="https://vitejs.dev" target="_blank">
      <div class="logo">
        <ImageLoader src={viteLogo} alt="Vite Logo" />
      </div>
    </Link>
    <Link href="https://svelte.dev" target="_blank">
      <div class="logo svelte">
        <ImageLoader src={svelteLogo} alt="Svelte Logo" />
      </div>
    </Link>
  </div>

  <h1>Vite + Svelte + Carbon</h1>

  <div class="card">
    <Counter />
  </div>

  <p>
    Check out <a
      href="https://github.com/sveltejs/kit#readme"
      target="_blank"
      rel="noreferrer">SvelteKit</a
    >, the official Svelte app framework powered by Vite!
  </p>

  <p class="read-the-docs">Click on the Vite and Svelte logos to learn more</p>
</Content>

<style>
  .card {
    padding: 2em;
  }

  .logo {
    height: 6em;
    padding: 1.5em;
    will-change: filter;
    transition: filter 300ms;
  }

  .logo:hover {
    filter: drop-shadow(0 0 2em #646cffaa);
  }

  .logo.svelte:hover {
    filter: drop-shadow(0 0 2em #ff3e00aa);
  }

  .read-the-docs {
    color: #888;
  }
</style>
