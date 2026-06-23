<script>
  import { base } from '$app/paths';
  import { page } from '$app/stores';
  import { onMount } from 'svelte';

  let scrolled = false;

  // Normalise the current path (strip the base prefix) for active-link matching.
  $: path = ($page.url.pathname || '/').replace(base, '') || '/';

  const links = [
    { href: '/',                 label: 'Home' },
    { href: '/chi-sono',         label: 'Chi sono' },
    { href: '/educazione-civica', label: 'Educazione civica' },
  ];

  onMount(() => {
    const onScroll = () => { scrolled = window.scrollY > 8; };
    onScroll();
    window.addEventListener('scroll', onScroll, { passive: true });
    return () => window.removeEventListener('scroll', onScroll);
  });
</script>

<nav class="nav" class:scrolled>
  <div class="nav__inner">
    <a class="brand" href="{base}/">Massano<span class="brand__dot">.</span></a>

    <input type="checkbox" id="nav-toggle" class="nav__toggle" aria-label="Apri menu" />

    <div class="nav__links">
      {#each links as l}
        <a class="nav__link" class:active={path === l.href} href="{base}{l.href}">{l.label}</a>
      {/each}
    </div>

    <label class="nav__burger" for="nav-toggle" aria-hidden="true">
      <span></span><span></span><span></span>
    </label>
  </div>
</nav>