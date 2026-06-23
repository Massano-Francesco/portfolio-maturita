<script>
  import { base } from '$app/paths';
  import { onMount } from 'svelte';
  import AnimatedBackground from '$lib/components/AnimatedBackground.svelte';

  let typed = '';
  let titleVisible = false;

  const fullTitle = 'Portfolio Digitale — Maturità Informatica';

  const sections = [
    { href: '/chi-sono', label: 'Chi Sono', desc: 'Il mio percorso e la mia storia', color: '#22d3ee' },
    { href: '/educazione-civica', label: 'Ed. Civica', desc: 'Cittadinanza digitale e consapevolezza', color: '#34d399' },
  ];

  onMount(() => {
    setTimeout(() => { titleVisible = true; }, 300);

    let i = 0;
    const typeInterval = setInterval(() => {
      if (i < fullTitle.length) {
        typed += fullTitle[i++];
      } else {
        clearInterval(typeInterval);
      }
    }, 40);

    return () => clearInterval(typeInterval);
  });
</script>

<svelte:head>
  <title>Portfolio F.E. Massano — Francesco Edoardo Massano</title>
</svelte:head>

<!-- Hero Section -->
<section class="hero">
  <AnimatedBackground variant="hero" />

  <div class="hero-content" class:visible={titleVisible}>
    <h1 class="hero-name reveal">
      <span class="name-pre">Francesco Edoardo</span>
      <span class="name-surname gradient-text">Massano</span>
    </h1>

    <div class="hero-title reveal">
      <span class="mono typing-text">{typed}<span class="cursor-blink">|</span></span>
    </div>

    <p class="hero-desc reveal">
      Studente di informatica con la passione per il codice, le architetture digitali e le nuove tecnologie.
      Questo spazio raccoglie il mio cammino dalla terza alla quinta superiore: un viaggio
      tra sviluppo software, reti, sistemi e crescita personale.
    </p>

    <div class="hero-cta reveal">
      <a href="{base}/chi-sono" class="btn-solid">
        Scopri il Percorso
        <span>→</span>
      </a>
      <a href="{base}/educazione-civica" class="btn-glow">
        Ed. Civica
      </a>
    </div>
  </div>

  <div class="hero-scroll">
    <span class="mono scroll-label">Scorri</span>
    <div class="scroll-arrow"></div>
  </div>
</section>

<!-- Preview sections -->
<section class="sections-preview section">
  <div class="container">
    <div class="section-label reveal">
      <span>Esplora il Portfolio</span>
    </div>
    <h2 class="preview-title reveal">
      Tre anni di studio,<br/><span class="gradient-text">un'identità da costruire</span>
    </h2>

    <div class="preview-grid">
      {#each sections as item, i}
        <a
          href={item.href}
          class="preview-card glass-card-hover reveal"
          style="animation-delay: {i * 0.1}s; --card-color: {item.color}"
        >
          <div class="card-content">
            <h3 class="card-title">{item.label}</h3>
            <p class="card-desc">{item.desc}</p>
          </div>
          <div class="card-arrow">→</div>
          <div class="card-glow" style="background: radial-gradient(circle at 50% 100%, {item.color}18, transparent 70%)"></div>
        </a>
      {/each}
    </div>
  </div>
</section>

<!-- About teaser -->
<section class="teaser-section section">
  <div class="container">
    <div class="teaser-inner">
      <div class="teaser-content reveal-left">
        <div class="section-label">Chi sono</div>
        <h2>Studente.<br/>Sviluppatore.<br/><span class="gradient-text">Curioso.</span></h2>
        <p class="teaser-text">
          Qui ho raccolto il mio percorso scolastico, i lavori realizzati e le competenze maturate
          durante gli anni all'Istituto Tecnico Edoardo Agnelli, indirizzo Informatica e Telecomunicazioni.
          Un cammino fatto di tecnologia, programmazione e continua crescita personale.
        </p>
        <a href="{base}/chi-sono" class="btn-glow" style="margin-top: 32px">Scopri di più →</a>
      </div>

      <div class="teaser-stats reveal-right">
        <div class="stat-card glass-card">
          <span class="stat-num gradient-text">3</span>
          <span class="stat-lab mono">Anni di studio</span>
        </div>
        <div class="stat-card glass-card">
          <span class="stat-num gradient-text">15+</span>
          <span class="stat-lab mono">Progetti</span>
        </div>
        <div class="stat-card glass-card">
          <span class="stat-num gradient-text">IT</span>
          <span class="stat-lab mono">Informatica &amp; TLC</span>
        </div>
        <div class="stat-card glass-card wide">
          <span class="mono stat-code">const portfolio = &#123; maturità: 2026 &#125;;</span>
        </div>
      </div>
    </div>
  </div>
</section>

<style>
  /* ─── HERO ─── */
  .hero {
    position: relative;
    min-height: 100vh;
    display: flex;
    align-items: center;
    padding: calc(var(--navbar-h, 72px) + 60px) 0 80px;
    overflow: hidden;
  }

  .hero-content {
    position: relative;
    z-index: 2;
    max-width: 1280px;
    margin: 0 auto;
    padding: 0 32px;
    display: flex;
    flex-direction: column;
    gap: 28px;
    opacity: 0;
    transform: translateY(20px);
    transition: all 0.8s cubic-bezier(0.4, 0, 0.2, 1);
  }

  .hero-content.visible { opacity: 1; transform: translateY(0); }

  .hero-name {
    font-size: clamp(3rem, 8vw, 7.5rem);
    font-weight: 800;
    line-height: 0.95;
    letter-spacing: -0.04em;
  }

  .name-pre { display: block; color: var(--text-primary); }

  .hero-title { min-height: 2rem; }

  .typing-text {
    font-size: clamp(0.9rem, 2vw, 1.1rem);
    color: var(--text-secondary);
    letter-spacing: 0.02em;
  }

  .cursor-blink {
    color: var(--accent-cyan);
    animation: blink 1s step-end infinite;
  }

  @keyframes blink {
    0%, 100% { opacity: 1; }
    50% { opacity: 0; }
  }

  .hero-desc {
    max-width: 600px;
    font-size: 1.05rem;
    color: var(--text-secondary);
    line-height: 1.7;
  }

  .hero-cta { display: flex; gap: 16px; flex-wrap: wrap; }

  .hero-scroll {
    position: absolute;
    bottom: 40px;
    left: 50%;
    transform: translateX(-50%);
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 8px;
    z-index: 2;
  }

  .scroll-label {
    font-size: 0.65rem;
    color: var(--text-muted);
    letter-spacing: 0.2em;
    text-transform: uppercase;
  }

  .scroll-arrow {
    width: 1px; height: 40px;
    background: linear-gradient(var(--accent-cyan), transparent);
    animation: scrollPulse 2s ease-in-out infinite;
  }

  @keyframes scrollPulse {
    0%, 100% { opacity: 1; transform: scaleY(1); }
    50% { opacity: 0.3; transform: scaleY(0.6); }
  }

  /* ─── PREVIEW GRID ─── */
  .preview-title {
    font-size: clamp(2rem, 5vw, 3.5rem);
    margin-bottom: 60px;
    max-width: 700px;
  }

  .preview-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
  }

  .preview-card {
    display: flex;
    align-items: center;
    gap: 20px;
    padding: 28px;
    position: relative;
    overflow: hidden;
    text-decoration: none;
    transition: all 0.35s cubic-bezier(0.4, 0, 0.2, 1);
  }

  .preview-card:hover {
    border-color: var(--card-color, var(--accent-cyan));
    transform: translateY(-6px);
    box-shadow: 0 20px 60px rgba(0,0,0,0.4), 0 0 30px color-mix(in srgb, var(--card-color, #22d3ee) 20%, transparent);
  }

  .card-content { flex: 1; }
  .card-title {
    font-family: var(--font-display);
    font-size: 1.1rem;
    font-weight: 700;
    color: var(--text-primary);
    margin-bottom: 6px;
  }

  .card-desc { font-size: 0.82rem; color: var(--text-muted); line-height: 1.5; }

  .card-arrow {
    color: var(--text-muted);
    font-size: 1.1rem;
    transition: all 0.3s;
    flex-shrink: 0;
  }

  .preview-card:hover .card-arrow {
    color: var(--card-color, var(--accent-cyan));
    transform: translateX(4px);
  }

  .card-glow {
    position: absolute; inset: 0;
    opacity: 0; transition: opacity 0.3s;
    pointer-events: none;
  }

  .preview-card:hover .card-glow { opacity: 1; }

  /* ─── TEASER ─── */
  .teaser-inner {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 60px;
    align-items: center;
  }

  .teaser-content { display: flex; flex-direction: column; gap: 20px; }

  .teaser-content h2 {
    font-size: clamp(2.5rem, 5vw, 4rem);
    line-height: 1.05;
  }

  .teaser-text {
    color: var(--text-secondary);
    line-height: 1.7;
    max-width: 520px;
  }

  .teaser-stats {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 16px;
  }

  .stat-card {
    padding: 28px 24px;
    display: flex;
    flex-direction: column;
    gap: 6px;
    transition: all 0.3s ease;
  }

  .stat-card:hover {
    border-color: var(--border-glow);
    transform: translateY(-4px);
  }

  .stat-card.wide {
    grid-column: span 2;
    padding: 20px 24px;
  }

  .stat-num {
    font-family: var(--font-display);
    font-size: 2.4rem;
    font-weight: 800;
    line-height: 1;
  }

  .stat-lab {
    font-size: 0.65rem;
    color: var(--text-muted);
    text-transform: uppercase;
    letter-spacing: 0.12em;
  }

  .stat-code {
    font-size: 0.78rem;
    color: var(--accent-cyan);
    opacity: 0.85;
  }

  @media (max-width: 768px) {
    .hero-content { padding: 0 20px; }
    .preview-grid { grid-template-columns: 1fr; }
    .teaser-inner { grid-template-columns: 1fr; gap: 40px; }
    .stat-card.wide { grid-column: span 1; }
  }
</style>
