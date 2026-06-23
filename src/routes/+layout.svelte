<script>
  import '../app.css';
  import Navbar from '$lib/components/Navbar.svelte';
  import Footer from '$lib/components/Footer.svelte';
  import { onMount } from 'svelte';

  onMount(() => {
    const revealObserver = new IntersectionObserver((entries) => {
      entries.forEach((entry, i) => {
        if (entry.isIntersecting) {
          setTimeout(() => {
            entry.target.classList.add('visible');
          }, i * 80);
        }
      });
    }, { threshold: 0.1 });

    const observeReveal = () => {
      document.querySelectorAll('.reveal, .reveal-left, .reveal-right').forEach(el => {
        revealObserver.observe(el);
      });
    };

    observeReveal();
    const mutObs = new MutationObserver(observeReveal);
    mutObs.observe(document.body, { childList: true, subtree: true });

    return () => {
      revealObserver.disconnect();
      mutObs.disconnect();
    };
  });
</script>

<Navbar />

<main>
  <slot />
</main>

<Footer />
