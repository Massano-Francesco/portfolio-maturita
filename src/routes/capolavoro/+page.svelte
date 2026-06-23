<script>
  import { base } from '$app/paths';
  import { onMount } from 'svelte';
  import AnimatedBackground from '$lib/components/AnimatedBackground.svelte';

  let heroVisible = false;

  const features = [
    { icon: '⚡', title: 'Performance', desc: 'Ottimizzato per velocità e scalabilità. Risposta in <100ms anche sotto carico.' },
    { icon: '🔐', title: 'Sicurezza', desc: 'Autenticazione JWT, crittografia end-to-end e protezione da vulnerabilità comuni.' },
    { icon: '📱', title: 'Responsive', desc: 'Funziona perfettamente su ogni dispositivo, da mobile a desktop ultra-wide.' },
    { icon: '🤖', title: 'AI-Powered', desc: '[Placeholder] Integrazione con AI per funzionalità intelligenti e personalizzazione.' },
    { icon: '☁️', title: 'Cloud Ready', desc: 'Architettura containerizzata, pronta per il deployment su cloud.' },
    { icon: '♿', title: 'Accessibile', desc: 'Rispetta gli standard WCAG 2.1 per l\'accessibilità universale.' },
  ];

  const stack = [
    { layer: 'Frontend', techs: ['React / Svelte', 'CSS3', 'TypeScript'] },
    { layer: 'Backend', techs: ['Node.js', 'Express', 'REST API'] },
    { layer: 'Database', techs: ['PostgreSQL', 'Redis'] },
    { layer: 'DevOps', techs: ['Docker', 'Git', 'CI/CD'] },
  ];

  const timeline = [
    { fase: 'Analisi', mese: 'Settembre 2024', desc: 'Studio dei requisiti, analisi del dominio e definizione degli obiettivi del progetto.' },
    { fase: 'Progettazione', mese: 'Ottobre 2024', desc: 'Architettura del sistema, design del database, wireframe UI/UX e documentazione tecnica.' },
    { fase: 'Sviluppo', mese: 'Nov 2024 – Feb 2025', desc: 'Implementazione iterativa con metodologia Agile. Sprint settimanali e review continue.' },
    { fase: 'Testing', mese: 'Marzo 2025', desc: 'Test unitari, di integrazione e test utente. Debug e ottimizzazione delle performance.' },
    { fase: 'Deploy', mese: 'Aprile 2025', desc: 'Deployment su cloud, configurazione del dominio e monitoraggio in produzione.' },
    { fase: 'Presentazione', mese: 'Giugno 2025', desc: 'Presentazione alla commissione di maturità. Il culmine di un percorso straordinario.' },
  ];

  onMount(() => {
    setTimeout(() => { heroVisible = true; }, 200);
  });
</script>

<svelte:head>
  <title>Capolavoro — Francesco Edoardo Massano</title>
</svelte:head>

<!-- CINEMATIC HERO -->
<section class="capo-hero" class:visible={heroVisible}>
  <AnimatedBackground variant="hero" />
  <div class="hero-overlay"></div>

  <!-- Floating code decorations -->
  <div class="code-deco">
    <span class="mono code-line cl1">const capolavoro = new Project();</span>
    <span class="mono code-line cl2">await deploy({'{'} env: 'production' {'}'});</span>
    <span class="mono code-line cl3">// Maturità 2025 ✓</span>
  </div>

  <div class="container hero-content">
    <div class="badge-wrap">
      <div class="hero-badge mono">⬡ Progetto Capolavoro 2025</div>
    </div>

    <h1 class="capo-title">
      <span class="title-line tl1">[Nome del</span>
      <span class="title-line tl2 gradient-text">Progetto]</span>
    </h1>

    <p class="capo-subtitle">
      [Placeholder] Sottotitolo del progetto — una frase che cattura l'essenza e
      il valore della soluzione sviluppata.
    </p>

    <div class="hero-actions">
      <a href="#overview" class="btn-solid">Scopri il Progetto</a>
      <a href="#tech-stack" class="btn-glow">Tech Stack →</a>
    </div>

    <div class="hero-meta">
      <div class="meta-item">
        <span class="mono meta-label">Durata</span>
        <span class="meta-value">8 mesi</span>
      </div>
      <div class="meta-div"></div>
      <div class="meta-item">
        <span class="mono meta-label">Tecnologie</span>
        <span class="meta-value">8+ Tools</span>
      </div>
      <div class="meta-div"></div>
      <div class="meta-item">
        <span class="mono meta-label">Status</span>
        <span class="meta-value" style="color: var(--accent-neon)">✓ Completato</span>
      </div>
    </div>
  </div>

  <div class="scroll-hint">
    <div class="scroll-line"></div>
  </div>
</section>

<!-- Overview -->
<section class="section" id="overview">
  <div class="container">
    <div class="overview-grid">
      <div class="overview-text reveal-left">
        <div class="section-label">Il Progetto</div>
        <h2>Cosa <span class="gradient-text">Risolve</span></h2>
        <p class="overview-para">
          <strong>[Placeholder]</strong> Descrivi qui il problema reale che il tuo progetto risolve.
          Qual è il contesto? Chi sono gli utenti? Perché questa soluzione è innovativa?
        </p>
        <p class="overview-para">
          Il progetto nasce dall'idea di... [continua con la descrizione del contesto,
          delle motivazioni e dell'impatto atteso della soluzione].
        </p>

        <div class="kpi-row">
          <div class="kpi-box">
            <span class="kpi-num glow-text">+X</span>
            <span class="kpi-lab mono">Feature principali</span>
          </div>
          <div class="kpi-box">
            <span class="kpi-num" style="color:var(--accent-violet-light)">Xk</span>
            <span class="kpi-lab mono">Linee di codice</span>
          </div>
          <div class="kpi-box">
            <span class="kpi-num" style="color:var(--accent-pink)">X</span>
            <span class="kpi-lab mono">Mesi di sviluppo</span>
          </div>
        </div>
      </div>

      <div class="overview-mockup reveal-right">
        <div class="mockup-frame">
          <div class="mockup-bar">
            <span class="mb-dot" style="background:#ff5f57"></span>
            <span class="mb-dot" style="background:#ffbd2e"></span>
            <span class="mb-dot" style="background:#28c840"></span>
            <span class="mb-url mono">[nome-progetto].app</span>
          </div>
          <div class="mockup-screen">
            <div class="ms-placeholder">
              <span class="ms-icon">🖥️</span>
              <span class="mono ms-text">[ Screenshot / Video del progetto ]</span>
              <span class="ms-sub">Inserire qui un'immagine o video demo</span>
            </div>
          </div>
        </div>
        <div class="mockup-glow"></div>
      </div>
    </div>
  </div>
</section>

<!-- Features -->
<section class="section features-section">
  <div class="container">
    <div class="section-label reveal">Caratteristiche</div>
    <h2 class="reveal">Feature <span class="gradient-text">Principali</span></h2>

    <div class="features-grid">
      {#each features as feat, i}
        <div class="feat-card glass-card-hover reveal" style="animation-delay:{i*0.08}s">
          <div class="feat-icon">{feat.icon}</div>
          <h3 class="feat-title">{feat.title}</h3>
          <p class="feat-desc">{feat.desc}</p>
        </div>
      {/each}
    </div>
  </div>
</section>

<!-- Tech Stack -->
<section class="section tech-section" id="tech-stack">
  <div class="container">
    <div class="section-label reveal">Tecnologie</div>
    <h2 class="reveal">Tech <span class="gradient-text">Stack</span></h2>

    <div class="stack-grid">
      {#each stack as layer, i}
        <div class="stack-layer reveal" style="animation-delay:{i*0.1}s">
          <div class="layer-label mono">{layer.layer}</div>
          <div class="layer-techs">
            {#each layer.techs as tech}
              <div class="tech-pill glass-card">{tech}</div>
            {/each}
          </div>
        </div>
      {/each}
    </div>
  </div>
</section>

<!-- Development timeline -->
<section class="section" style="background: var(--bg-secondary)">
  <div class="container">
    <div class="section-label reveal">Sviluppo</div>
    <h2 class="reveal">Come è <span class="gradient-text">Nato</span></h2>

    <div class="dev-timeline">
      {#each timeline as fase, i}
        <div class="dt-item reveal" style="animation-delay:{i*0.1}s">
          <div class="dt-num mono">{String(i+1).padStart(2,'0')}</div>
          <div class="dt-body glass-card">
            <div class="dt-header">
              <h3>{fase.fase}</h3>
              <span class="mono dt-date">{fase.mese}</span>
            </div>
            <p>{fase.desc}</p>
          </div>
          {#if i < timeline.length - 1}
            <div class="dt-connector"></div>
          {/if}
        </div>
      {/each}
    </div>
  </div>
</section>

<!-- CTA final -->
<section class="section cta-final">
  <AnimatedBackground />
  <div class="container cta-content reveal">
    <h2>Pronto a vederlo<br/><span class="gradient-text">dal vivo?</span></h2>
    <p>Visita il repository GitHub o contattami per una demo dal vivo del progetto.</p>
    <div class="cta-actions">
      <a href="https://github.com" target="_blank" class="btn-solid">GitHub Repository →</a>
      <a href="{base}/contatti" class="btn-glow">Contattami</a>
    </div>
  </div>
</section>

<style>
  /* ─── CINEMATIC HERO ─── */
  .capo-hero {
    position: relative;
    min-height: 100vh;
    display: flex;
    align-items: center;
    padding: calc(var(--navbar-h,72px) + 80px) 0 100px;
    overflow: hidden;
  }

  .hero-overlay {
    position: absolute;
    inset: 0;
    background: radial-gradient(ellipse at 60% 40%, rgba(34, 211, 238, 0.15) 0%, transparent 60%),
                radial-gradient(ellipse at 20% 80%, rgba(0, 212, 255, 0.1) 0%, transparent 50%);
    pointer-events: none;
  }

  /* Floating code decorations */
  .code-deco {
    position: absolute;
    inset: 0;
    pointer-events: none;
    overflow: hidden;
  }

  .code-line {
    position: absolute;
    font-size: 0.75rem;
    color: var(--text-muted);
    opacity: 0.3;
    white-space: nowrap;
  }

  .cl1 { top: 25%; right: 8%; animation: floatCode 8s ease-in-out infinite; }
  .cl2 { top: 45%; right: 5%; animation: floatCode 10s ease-in-out infinite 2s; }
  .cl3 { top: 65%; right: 12%; animation: floatCode 6s ease-in-out infinite 4s; }

  @keyframes floatCode {
    0%, 100% { transform: translateY(0); opacity: 0.3; }
    50% { transform: translateY(-10px); opacity: 0.6; }
  }

  .hero-content {
    position: relative;
    z-index: 2;
    display: flex;
    flex-direction: column;
    gap: 32px;
  }

  .badge-wrap {
    opacity: 0;
    animation: fadeInUp 0.6s 0.3s forwards;
  }

  .hero-badge {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 8px 20px;
    border: 1px solid rgba(34, 211, 238, 0.4);
    border-radius: 100px;
    font-size: 0.8rem;
    color: var(--accent-violet-light);
    background: rgba(34, 211, 238, 0.08);
    width: fit-content;
  }

  .capo-title {
    display: flex;
    flex-direction: column;
    font-size: clamp(4rem, 10vw, 9rem);
    line-height: 0.95;
    letter-spacing: -0.04em;
  }

  .title-line {
    display: block;
    opacity: 0;
    transform: translateY(40px);
  }

  .tl1 { animation: fadeInUp 0.8s 0.4s forwards; }
  .tl2 { animation: fadeInUp 0.8s 0.55s forwards; }

  @keyframes fadeInUp {
    to { opacity: 1; transform: translateY(0); }
  }

  .capo-subtitle {
    max-width: 560px;
    font-size: 1.1rem;
    color: var(--text-secondary);
    line-height: 1.7;
    opacity: 0;
    animation: fadeInUp 0.8s 0.7s forwards;
  }

  .hero-actions {
    display: flex;
    gap: 16px;
    flex-wrap: wrap;
    opacity: 0;
    animation: fadeInUp 0.8s 0.85s forwards;
  }

  .hero-meta {
    display: flex;
    align-items: center;
    gap: 32px;
    opacity: 0;
    animation: fadeInUp 0.8s 1s forwards;
    flex-wrap: wrap;
  }

  .meta-item { display: flex; flex-direction: column; gap: 4px; }
  .meta-label { font-size: 0.65rem; color: var(--text-muted); text-transform: uppercase; letter-spacing: 0.15em; }
  .meta-value { font-size: 1rem; font-weight: 600; font-family: var(--font-display); }
  .meta-div { width: 1px; height: 40px; background: var(--border-subtle); }

  .scroll-hint {
    position: absolute;
    bottom: 40px;
    left: 50%;
    transform: translateX(-50%);
    z-index: 2;
  }

  .scroll-line {
    width: 1px; height: 60px;
    background: linear-gradient(var(--accent-cyan), transparent);
    margin: 0 auto;
    animation: scrollPulse 2s ease-in-out infinite;
  }

  @keyframes scrollPulse {
    0%, 100% { opacity: 1; transform: scaleY(1); }
    50% { opacity: 0.3; transform: scaleY(0.5); }
  }

  /* ─── OVERVIEW ─── */
  .overview-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 80px;
    align-items: center;
  }

  .overview-text { display: flex; flex-direction: column; gap: 20px; }
  .overview-text h2 { font-size: clamp(2rem, 4vw, 3.5rem); }
  .overview-para { font-size: 1rem; color: var(--text-secondary); line-height: 1.8; }

  .kpi-row {
    display: flex;
    gap: 32px;
    margin-top: 8px;
  }

  .kpi-box { display: flex; flex-direction: column; gap: 4px; }

  .kpi-num {
    font-family: var(--font-display);
    font-size: 2.5rem;
    font-weight: 800;
    line-height: 1;
    color: var(--accent-cyan);
    text-shadow: var(--glow-text);
  }

  .kpi-lab {
    font-size: 0.7rem;
    color: var(--text-muted);
    text-transform: uppercase;
    letter-spacing: 0.1em;
  }

  /* Mockup */
  .overview-mockup { position: relative; }

  .mockup-frame {
    border-radius: var(--radius-md);
    overflow: hidden;
    border: 1px solid var(--border-subtle);
    background: var(--bg-secondary);
    position: relative;
    z-index: 2;
  }

  .mockup-bar {
    display: flex;
    align-items: center;
    gap: 8px;
    padding: 12px 16px;
    border-bottom: 1px solid var(--border-subtle);
    background: var(--bg-card);
  }

  .mb-dot { width: 10px; height: 10px; border-radius: 50%; }

  .mb-url {
    margin-left: 12px;
    font-size: 0.7rem;
    color: var(--text-muted);
    flex: 1;
    text-align: center;
  }

  .mockup-screen {
    aspect-ratio: 16/10;
    display: flex;
    align-items: center;
    justify-content: center;
    background: var(--bg-primary);
    position: relative;
  }

  .ms-placeholder {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 12px;
    color: var(--text-muted);
    text-align: center;
    padding: 40px;
  }

  .ms-icon { font-size: 3rem; }
  .ms-text { font-size: 0.8rem; letter-spacing: 0.1em; text-transform: uppercase; }
  .ms-sub { font-size: 0.75rem; color: var(--text-muted); opacity: 0.6; }

  .mockup-glow {
    position: absolute;
    inset: -20px;
    background: radial-gradient(ellipse at 50% 50%, rgba(34, 211, 238, 0.15), transparent 70%);
    z-index: 1;
    pointer-events: none;
  }

  /* Features */
  .features-section { background: var(--bg-secondary); }

  .features-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
  }

  .feat-card {
    padding: 28px;
    display: flex;
    flex-direction: column;
    gap: 12px;
  }

  .feat-icon { font-size: 2rem; }
  .feat-title { font-size: 1.05rem; }
  .feat-desc { font-size: 0.85rem; color: var(--text-muted); line-height: 1.6; }

  /* Stack */
  .stack-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 20px;
    margin-top: 48px;
  }

  .stack-layer {
    display: flex;
    flex-direction: column;
    gap: 16px;
  }

  .layer-label {
    font-size: 0.7rem;
    color: var(--accent-cyan);
    text-transform: uppercase;
    letter-spacing: 0.2em;
    padding-bottom: 8px;
    border-bottom: 1px solid var(--border-glow);
  }

  .layer-techs {
    display: flex;
    flex-direction: column;
    gap: 8px;
  }

  .tech-pill {
    padding: 10px 16px;
    font-size: 0.85rem;
    font-family: var(--font-mono);
    color: var(--text-secondary);
    text-align: center;
    transition: all 0.2s;
  }

  .tech-pill:hover {
    border-color: var(--accent-cyan);
    color: var(--accent-cyan);
    box-shadow: 0 0 12px rgba(0,212,255,0.15);
  }

  /* Dev timeline */
  .dev-timeline {
    display: flex;
    flex-direction: column;
    gap: 4px;
    margin-top: 48px;
  }

  .dt-item {
    display: grid;
    grid-template-columns: 48px 1fr;
    gap: 20px;
    position: relative;
  }

  .dt-num {
    font-size: 1.2rem;
    font-weight: 700;
    color: var(--text-muted);
    padding-top: 20px;
    text-align: center;
  }

  .dt-body {
    padding: 24px;
    margin-bottom: 12px;
  }

  .dt-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 10px;
    flex-wrap: wrap;
    gap: 8px;
  }

  .dt-header h3 { font-size: 1.05rem; }

  .dt-date {
    font-size: 0.75rem;
    color: var(--accent-cyan);
    opacity: 0.8;
  }

  .dt-body p {
    font-size: 0.9rem;
    color: var(--text-muted);
    line-height: 1.6;
  }

  /* CTA Final */
  .cta-final {
    position: relative;
    text-align: center;
    border-top: 1px solid var(--border-subtle);
  }

  .cta-content {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 24px;
    position: relative;
    z-index: 2;
  }

  .cta-content h2 { font-size: clamp(2.5rem, 6vw, 5rem); }
  .cta-content p { color: var(--text-secondary); font-size: 1.05rem; max-width: 500px; }

  .cta-actions { display: flex; gap: 16px; flex-wrap: wrap; justify-content: center; }

  /* Section titles */
  .section h2 { font-size: clamp(2rem, 4vw, 3.2rem); margin-bottom: 48px; }

  @media (max-width: 1024px) {
    .stack-grid { grid-template-columns: repeat(2, 1fr); }
    .features-grid { grid-template-columns: repeat(2, 1fr); }
  }

  @media (max-width: 768px) {
    .overview-grid { grid-template-columns: 1fr; gap: 40px; }
    .features-grid { grid-template-columns: 1fr; }
    .stack-grid { grid-template-columns: repeat(2, 1fr); }
    .kpi-row { gap: 20px; }
    .hero-meta { gap: 16px; }
  }

  @media (max-width: 480px) {
    .capo-title { font-size: clamp(3rem, 14vw, 5rem); }
    .stack-grid { grid-template-columns: 1fr; }
  }
</style>
