<script>
  import { base } from '$app/paths';
  import { page } from '$app/stores';
  import { onMount } from 'svelte';

  let menuOpen = false;
  let scrolled = false;

  const navItems = [
    { href: `${base}/`, label: 'Home', code: '00' },
    { href: `${base}/chi-sono`, label: 'Chi Sono', code: '01' },
    { href: `${base}/educazione-civica`, label: 'Ed. Civica', code: '02' },
  ];

  onMount(() => {
    const handleScroll = () => { scrolled = window.scrollY > 20; };
    window.addEventListener('scroll', handleScroll);
    return () => window.removeEventListener('scroll', handleScroll);
  });

  function closeMenu() { menuOpen = false; }
  function toggleMenu() { menuOpen = !menuOpen; }

  $: activePath = $page.url.pathname;
</script>

<nav class="navbar" class:scrolled>
  <div class="nav-inner">
    <!-- Logo -->
    <a href="{base}/" class="nav-logo" on:click={closeMenu}>
      <span class="logo-bracket">&lt;</span>
      <span class="logo-text">FM</span>
      <span class="logo-bracket">/&gt;</span>
    </a>

    <!-- Desktop nav -->
    <ul class="nav-links">
      {#each navItems as item}
        <li>
          <a
            href={item.href}
            class="nav-link"
            class:active={activePath === item.href || (item.href !== '/' && activePath.startsWith(item.href))}
          >
            <span class="nav-code">{item.code}</span>
            {item.label}
          </a>
        </li>
      {/each}
    </ul>

    <!-- Hamburger -->
    <button class="hamburger" on:click={toggleMenu} aria-label="Menu" class:open={menuOpen}>
      <span></span>
      <span></span>
      <span></span>
    </button>
  </div>
</nav>

<!-- Mobile fullscreen menu -->
<div class="fullscreen-menu" class:open={menuOpen}>
  <div class="menu-bg-decoration">
    <div class="deco-circle c1"></div>
    <div class="deco-circle c2"></div>
  </div>
  <nav class="full-nav">
    {#each navItems as item, i}
      <a
        href={item.href}
        class="full-nav-link"
        class:active={activePath === item.href}
        on:click={closeMenu}
        style="animation-delay: {i * 0.06}s"
      >
        <span class="full-nav-code">{item.code}.</span>
        <span class="full-nav-label">{item.label}</span>
        <span class="full-nav-arrow">→</span>
      </a>
    {/each}
  </nav>
</div>

<style>
  .navbar {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 1000;
    height: var(--navbar-h, 72px);
    transition: background 0.3s ease, backdrop-filter 0.3s ease, border-color 0.3s;
    border-bottom: 1px solid transparent;
  }

  .navbar.scrolled {
    background: rgba(2, 4, 8, 0.85);
    backdrop-filter: blur(24px);
    -webkit-backdrop-filter: blur(24px);
    border-bottom-color: var(--border-subtle, rgba(255,255,255,0.06));
  }

  .nav-inner {
    max-width: 1280px;
    margin: 0 auto;
    padding: 0 32px;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .nav-logo {
    font-family: var(--font-display);
    font-size: 1.4rem;
    font-weight: 800;
    letter-spacing: -0.02em;
    display: flex;
    align-items: center;
    gap: 2px;
    transition: all 0.2s;
  }

  .logo-bracket {
    color: var(--accent-cyan);
    text-shadow: var(--glow-text);
  }

  .logo-text {
    color: var(--text-primary);
  }

  .nav-logo:hover .logo-text {
    color: var(--accent-cyan);
  }

  .nav-links {
    display: flex;
    list-style: none;
    gap: 4px;
  }

  .nav-link {
    display: flex;
    align-items: center;
    gap: 6px;
    padding: 8px 14px;
    border-radius: 6px;
    font-family: var(--font-body);
    font-size: 0.875rem;
    font-weight: 500;
    color: var(--text-secondary);
    transition: all 0.2s;
    position: relative;
  }

  .nav-link::after {
    content: '';
    position: absolute;
    bottom: 4px;
    left: 50%;
    transform: translateX(-50%) scaleX(0);
    width: 60%;
    height: 1px;
    background: var(--accent-cyan);
    box-shadow: 0 0 6px var(--accent-cyan);
    transition: transform 0.25s cubic-bezier(0.4, 0, 0.2, 1);
  }

  .nav-link:hover { color: var(--text-primary); }
  .nav-link.active { color: var(--accent-cyan); }
  .nav-link.active::after,
  .nav-link:hover::after { transform: translateX(-50%) scaleX(1); }

  .nav-code {
    font-family: var(--font-mono);
    font-size: 0.65rem;
    color: var(--accent-cyan);
    opacity: 0.6;
  }

  /* Hamburger */
  .hamburger {
    display: none;
    flex-direction: column;
    gap: 6px;
    background: none;
    border: none;
    padding: 8px;
    z-index: 1100;
    position: relative;
    cursor: pointer;
  }

  .hamburger span {
    display: block;
    width: 28px;
    height: 1.5px;
    background: var(--text-primary);
    border-radius: 1px;
    transition: all 0.35s cubic-bezier(0.4, 0, 0.2, 1);
    transform-origin: center;
  }

  .hamburger.open span:nth-child(1) {
    transform: translateY(7.5px) rotate(45deg);
    background: var(--accent-cyan);
  }

  .hamburger.open span:nth-child(2) {
    opacity: 0;
    transform: scaleX(0);
  }

  .hamburger.open span:nth-child(3) {
    transform: translateY(-7.5px) rotate(-45deg);
    background: var(--accent-cyan);
  }

  /* Fullscreen menu */
  .fullscreen-menu {
    position: fixed;
    inset: 0;
    background: rgba(2, 4, 8, 0.97);
    z-index: 999;
    display: flex;
    align-items: center;
    justify-content: center;
    opacity: 0;
    visibility: hidden;
    transition: opacity 0.4s ease, visibility 0.4s ease;
    overflow: hidden;
  }

  .fullscreen-menu.open {
    opacity: 1;
    visibility: visible;
  }

  .menu-bg-decoration {
    position: absolute;
    inset: 0;
    pointer-events: none;
  }

  .deco-circle {
    position: absolute;
    border-radius: 50%;
    filter: blur(80px);
  }

  .c1 {
    width: 400px; height: 400px;
    background: rgba(34, 211, 238, 0.08);
    top: -100px; right: -100px;
  }

  .c2 {
    width: 300px; height: 300px;
    background: rgba(52, 211, 153, 0.1);
    bottom: -50px; left: -50px;
  }

  .full-nav {
    display: flex;
    flex-direction: column;
    gap: 8px;
    width: 100%;
    max-width: 500px;
    padding: 0 40px;
  }

  .full-nav-link {
    display: flex;
    align-items: center;
    gap: 16px;
    padding: 18px 0;
    border-bottom: 1px solid var(--border-subtle);
    font-family: var(--font-display);
    font-size: 2rem;
    font-weight: 700;
    color: var(--text-secondary);
    transition: all 0.25s;
    opacity: 0;
    transform: translateX(-30px);
  }

  .fullscreen-menu.open .full-nav-link {
    animation: slideInLeft 0.4s forwards;
  }

  @keyframes slideInLeft {
    to { opacity: 1; transform: translateX(0); }
  }

  .full-nav-link:hover,
  .full-nav-link.active {
    color: var(--text-primary);
    border-bottom-color: var(--accent-cyan);
  }

  .full-nav-link:hover .full-nav-code {
    color: var(--accent-cyan);
  }

  .full-nav-code {
    font-family: var(--font-mono);
    font-size: 0.85rem;
    color: var(--text-muted);
    min-width: 32px;
    transition: color 0.2s;
  }

  .full-nav-label { flex: 1; }

  .full-nav-arrow {
    font-size: 1.2rem;
    color: var(--text-muted);
    transform: translateX(-8px);
    transition: all 0.25s;
    opacity: 0;
  }

  .full-nav-link:hover .full-nav-arrow {
    color: var(--accent-cyan);
    transform: translateX(0);
    opacity: 1;
  }

  @media (max-width: 900px) {
    .nav-links { display: none; }
    .hamburger { display: flex; }
  }

  @media (max-width: 480px) {
    .nav-inner { padding: 0 20px; }
    .full-nav { padding: 0 24px; }
    .full-nav-link { font-size: 1.5rem; }
  }
</style>