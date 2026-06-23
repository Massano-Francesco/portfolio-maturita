<script>
  import { base } from '$app/paths';
  import AnimatedBackground from '$lib/components/AnimatedBackground.svelte';
</script>

<svelte:head>
  <title>Francesco Edoardo Massano — Portfolio Maturità</title>
  <meta
    name="description"
    content="Portfolio digitale di Francesco Edoardo Massano, studente di Informatica e Telecomunicazioni all'ITIS Edoardo Agnelli di Torino. Esame di Stato 2026." />
</svelte:head>

<!-- ───────────────────────── HERO ───────────────────────── -->
<section class="hero">
  <AnimatedBackground variant="hero" />

  <div class="container">
    <div class="hero__inner">
      <span class="eyebrow rise" style="--d:.05s">Portfolio digitale · Esame di Stato 2026</span>

      <h1 class="hero__name">
        <span class="l1 rise" style="--d:.16s">Francesco Edoardo</span>
        <span class="l2 rise" style="--d:.26s">Massano<span class="dot">.</span></span>
      </h1>

      <p class="hero__lead rise" style="--d:.4s">
        Cinque anni all'Istituto Edoardo Agnelli, raccolti in un unico luogo. Non un elenco
        di voti, ma le cose che ho <em>costruito</em>, gli errori che mi hanno insegnato
        qualcosa e l'idea — sempre più chiara — di chi voglio diventare.
      </p>

      <div class="hero__cta rise" style="--d:.52s">
        <a class="btn btn--primary" href="{base}/chi-sono">Il mio percorso <span class="arrow">→</span></a>
        <a class="btn btn--ghost" href="{base}/educazione-civica">Educazione civica</a>
      </div>

      <div class="hero__meta rise" style="--d:.64s">
        <span>Indirizzo <b>Informatica &amp; Telecomunicazioni</b></span>
        <span>Sede <b>ITIS E. Agnelli, Torino</b></span>
        <span>Anno <b>2025 / 26</b></span>
      </div>
    </div>
  </div>

  <div class="hero__scroll">
    <span class="hero__scroll-line"></span>
    Scorri
  </div>
</section>

<!-- ──────────────────────── INDICE ──────────────────────── -->
<section class="section">
  <div class="container">
    <div class="head reveal">
      <span class="eyebrow">Indice</span>
      <h2 class="head__title">Due sezioni,<br />un percorso da raccontare.</h2>
    </div>

    <div class="index">
      <a class="index__row reveal" href="{base}/chi-sono">
        <span class="index__num">01</span>
        <span>
          <span class="index__title">Chi sono</span>
          <span class="index__desc">
            La persona dietro il portfolio: dalla terza alla quinta, le competenze
            costruite e ciò che mi spinge a creare.
          </span>
        </span>
        <span class="index__arrow">→</span>
      </a>

      <a class="index__row reveal" href="{base}/educazione-civica">
        <span class="index__num">02</span>
        <span>
          <span class="index__title">Educazione civica</span>
          <span class="index__desc">
            Cittadinanza digitale: vivere la rete con diritti, doveri e una buona dose
            di consapevolezza.
          </span>
        </span>
        <span class="index__arrow">→</span>
      </a>
    </div>
  </div>
</section>

<!-- ─────────────────────── IN BREVE ─────────────────────── -->
<section class="section section--tight section--panel">
  <div class="container">
    <span class="eyebrow reveal" style="margin-bottom:34px;display:inline-flex">In breve</span>
    <div class="facts reveal">
      <div class="fact"><div class="fact__k">Indirizzo</div><div class="fact__v">Informatica &amp; TLC</div></div>
      <div class="fact"><div class="fact__k">Istituto</div><div class="fact__v">ITIS E. Agnelli</div></div>
      <div class="fact"><div class="fact__k">Sede</div><div class="fact__v">Torino</div></div>
      <div class="fact"><div class="fact__k">Esame</div><div class="fact__v">Maturità 2026</div></div>
    </div>
  </div>
</section>

<!-- ──────────────────────── TEASER ──────────────────────── -->
<section class="section">
  <div class="container">
    <div class="teaser__grid">
      <div class="reveal-left">
        <span class="eyebrow">Il metodo</span>
        <h2 class="teaser__title">Imparo<br />costruendo.</h2>
        <p class="teaser__text">
          Mi piace partire da un problema reale e arrivare a qualcosa che funziona davvero:
          un sito, uno script, una rete che parla. La scuola mi ha dato gli strumenti;
          la curiosità ha fatto il resto.
        </p>
        <a class="link-arrow" href="{base}/chi-sono">Conosci la mia storia <span class="arrow">→</span></a>
      </div>

      <div class="teaser__card reveal-right">
        <p class="teaser__quote">
          <span class="mark">“</span>
          La parte difficile non è scrivere codice. È capire cosa vale davvero la pena
          costruire.
        </p>
        <div class="teaser__sign">Francesco Edoardo Massano</div>
      </div>
    </div>
  </div>
</section>