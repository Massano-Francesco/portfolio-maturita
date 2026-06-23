<script>
  import { base } from '$app/paths';
  import AnimatedBackground from '$lib/components/AnimatedBackground.svelte';

  const infoItems = [
    { label: 'Scuola', value: 'Istituto Tecnico Edoardo Agnelli' },
    { label: 'Indirizzo', value: 'Informatica e Telecomunicazioni' },
    { label: 'Anno', value: '2025/2026' },
    { label: 'Classe', value: '5° ITT' },
  ];

  const skills = ['C', 'Python', 'Pygame', 'Tkinter', 'Reti', 'Database', 'Linux'];
</script>

<svelte:head>
  <title>Chi Sono — Francesco Edoardo Massano</title>
</svelte:head>

<!-- Hero -->
<section class="page-hero">
  <AnimatedBackground />
  <div class="hero-inner container">
    <div class="section-label reveal">01 / Chi Sono</div>
    <h1 class="reveal">
      Presentazione<br/>
      <span class="gradient-text">Personale</span>
    </h1>
    <p class="hero-sub reveal">Una finestra sul mio percorso, sulle mie passioni e su dove voglio arrivare.</p>
  </div>
</section>

<!-- Main content -->
<section class="section">
  <div class="container">
    <div class="info-strip reveal">
      {#each infoItems as item}
        <div class="info-pill glass-card">
          <span class="info-label mono">{item.label}</span>
          <span class="info-value">{item.value}</span>
        </div>
      {/each}
    </div>

    <div class="profile-content">
      <div class="profile-text">
        <div class="section-label reveal">Descrizione</div>
        <h2 class="reveal">Ciao, sono<br/><span class="glow-text">Francesco Edoardo Massano</span></h2>

        <p class="bio reveal">
          Sono Francesco Edoardo Massano, studente del quinto anno all'Istituto Tecnico Edoardo Agnelli
          nell'indirizzo Informatica e Telecomunicazioni.

          Ho sempre trovato nell'informatica qualcosa di più di una materia scolastica: un modo di pensare,
          di risolvere problemi, di dare forma alle idee. Nel corso degli anni ho approfondito la programmazione,
          le reti, i sistemi operativi, la cybersecurity e i database, costruendo passo dopo passo
          una visione più completa del mondo digitale.

          Questo portfolio è la mia storia raccontata attraverso i progetti e le esperienze vissute:
          non solo quello che ho imparato, ma come mi ha cambiato. Ogni lavoro qui presente è un tassello
          di un percorso fatto di curiosità, tentativi e soddisfazioni.

          La tecnologia per me è uno strumento creativo: trasforma idee astratte in qualcosa di concreto
          e funzionante. È questo che mi spinge a continuare a imparare e a mettermi in gioco.
        </p>

        <p class="bio reveal">
          In questi tre anni ho capito che programmare non significa solo scrivere codice: significa
          ragionare con metodo, affrontare l'errore come parte del processo e trovare soluzioni
          eleganti a problemi reali. Il mio obiettivo è crescere nel settore tech, esplorare nuovi
          linguaggi e paradigmi, e contribuire a progetti che abbiano un impatto concreto.
        </p>
      </div>

      <aside class="profile-aside reveal-right">
        <div class="skills-card glass-card">
          <span class="mono skills-title">Competenze</span>
          <div class="skills-tags">
            {#each skills as skill}
              <span class="skill-tag">{skill}</span>
            {/each}
          </div>
        </div>

        <div class="quote-card glass-card">
          <span class="mono quote-label">// motivazione</span>
          <p class="quote-text">"Il codice è poesia che la macchina può eseguire."</p>
        </div>
      </aside>
    </div>
  </div>
</section>

<style>
  .page-hero {
    position: relative;
    min-height: 50vh;
    display: flex;
    align-items: flex-end;
    padding: calc(var(--navbar-h,72px) + 60px) 0 80px;
    overflow: hidden;
    border-bottom: 1px solid var(--border-subtle);
  }

  .hero-inner h1 { font-size: clamp(3rem, 7vw, 6rem); margin-bottom: 16px; }
  .hero-sub { font-size: 1.05rem; color: var(--text-secondary); max-width: 500px; }

  .info-strip {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 16px;
    margin-bottom: 64px;
  }

  .info-pill {
    padding: 18px 20px;
    display: flex;
    flex-direction: column;
    gap: 6px;
    transition: all 0.3s ease;
  }

  .info-pill:hover {
    border-color: var(--border-glow);
    transform: translateY(-3px);
  }

  .info-label {
    font-size: 0.65rem;
    color: var(--accent-cyan);
    text-transform: uppercase;
    letter-spacing: 0.12em;
  }

  .info-value {
    font-size: 0.88rem;
    color: var(--text-primary);
    font-weight: 500;
    line-height: 1.4;
  }

  .profile-content {
    display: grid;
    grid-template-columns: 1fr 320px;
    gap: 60px;
    align-items: start;
  }

  .profile-text { display: flex; flex-direction: column; gap: 24px; }
  .profile-text h2 { font-size: clamp(2rem, 4vw, 3rem); }

  .bio {
    font-size: 1rem;
    color: var(--text-secondary);
    line-height: 1.8;
    white-space: pre-line;
  }

  .profile-aside {
    display: flex;
    flex-direction: column;
    gap: 20px;
    position: sticky;
    top: 100px;
  }

  .skills-card {
    padding: 24px;
    display: flex;
    flex-direction: column;
    gap: 16px;
  }

  .skills-title {
    font-size: 0.68rem;
    color: var(--text-muted);
    text-transform: uppercase;
    letter-spacing: 0.15em;
  }

  .skills-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }

  .skill-tag {
    padding: 6px 14px;
    background: rgba(34, 211, 238, 0.08);
    border: 1px solid rgba(34, 211, 238, 0.2);
    border-radius: 100px;
    font-family: var(--font-mono);
    font-size: 0.72rem;
    color: var(--accent-cyan);
  }

  .quote-card {
    padding: 24px;
    border-left: 3px solid var(--accent-neon);
  }

  .quote-label {
    font-size: 0.65rem;
    color: var(--text-muted);
    display: block;
    margin-bottom: 12px;
  }

  .quote-text {
    font-size: 0.95rem;
    color: var(--text-secondary);
    font-style: italic;
    line-height: 1.6;
  }

  @media (max-width: 900px) {
    .info-strip { grid-template-columns: repeat(2, 1fr); }
    .profile-content { grid-template-columns: 1fr; }
    .profile-aside { position: static; }
  }

  @media (max-width: 480px) {
    .info-strip { grid-template-columns: 1fr; }
  }
</style>
