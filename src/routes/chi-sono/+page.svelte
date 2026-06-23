<script>
  import { base } from '$app/paths';
</script>

<svelte:head>
  <title>Chi sono — Francesco Edoardo Massano</title>
  <meta
    name="description"
    content="Chi è Francesco Edoardo Massano: il percorso dalla terza alla quinta in Informatica e Telecomunicazioni, le competenze e gli interessi." />
</svelte:head>

<!-- ─────────────────────── ABOUT HERO ─────────────────────── -->
<section class="about-hero section--tight">
  <div class="container">
    <span class="eyebrow rise" style="--d:.05s">Chi sono</span>
    <h1 class="about-hero__title rise" style="--d:.16s">
      Costruisco cose che prima non c'erano<span class="dot">.</span>
    </h1>
    <p class="lead about-hero__lead rise" style="--d:.32s">
      Mi chiamo Francesco Edoardo Massano. Sto concludendo cinque anni di Informatica e
      Telecomunicazioni all'Istituto Edoardo Agnelli di Torino, e questo portfolio è il modo
      in cui ho scelto di raccontarmi: <em>con i fatti, non con le parole di circostanza.</em>
    </p>
  </div>
</section>

<hr class="rule" style="max-width:var(--maxw);margin-inline:auto" />

<!-- ─────────────────────── NARRATIVE ─────────────────────── -->
<section class="section">
  <div class="container">
    <div class="editorial reveal">
      <div class="editorial__label">Il punto di partenza</div>
      <div class="prose">
        <p>
          Mi sono avvicinato alla programmazione quasi per caso, e ci sono rimasto per una
          ragione semplice: mi piace la sensazione di trasformare un'idea in qualcosa che
          funziona. Da lì è venuto naturale interessarmi a tutto il resto — come si tengono
          in piedi le <strong>reti</strong>, come comunicano i <strong>sistemi</strong>, come
          si progetta qualcosa pensando davvero a chi dovrà usarlo.
        </p>
        <p>
          Negli anni ho capito che la parte tecnica è solo metà del lavoro. L'altra metà è
          il contesto: le persone, gli obiettivi, il <span class="accent">perché</span>. È
          per questo che, oltre al codice, mi interessano il design, l'imprenditoria e tutto
          ciò che vive nel punto in cui la tecnologia incontra la vita reale.
        </p>
      </div>
    </div>

    <div class="editorial reveal">
      <div class="editorial__label">Il percorso</div>
      <div class="path">
        <div class="path__item">
          <div class="path__rail"><span class="path__dot"></span><span class="path__stem"></span></div>
          <div>
            <div class="path__year">Terza · le fondamenta</div>
            <div class="path__h">Imparare a pensare in codice</div>
            <p class="path__d">
              I primi linguaggi, la logica, gli algoritmi. Il momento in cui un programma
              gira per la prima volta e capisci che puoi costruire qualunque cosa.
            </p>
          </div>
        </div>

        <div class="path__item">
          <div class="path__rail"><span class="path__dot"></span><span class="path__stem"></span></div>
          <div>
            <div class="path__year">Quarta · la struttura</div>
            <div class="path__h">Reti, sistemi e progetti veri</div>
            <p class="path__d">
              Dal singolo programma all'architettura: reti, database, sistemi che dialogano.
              Progetti più ambiziosi, lavoro in gruppo e i primi problemi senza soluzione
              pronta sul libro.
            </p>
          </div>
        </div>

        <div class="path__item">
          <div class="path__rail"><span class="path__dot"></span><span class="path__stem"></span></div>
          <div>
            <div class="path__year">Quinta · la sintesi</div>
            <div class="path__h">Mettere tutto insieme</div>
            <p class="path__d">
              L'anno in cui i pezzi si uniscono: l'Esame di Stato, questo portfolio e i
              primi passi oltre la scuola, con uno sguardo già rivolto a quello che viene dopo.
            </p>
          </div>
        </div>
      </div>
    </div>

    <div class="editorial reveal">
      <div class="editorial__label">Competenze</div>
      <div>
        <div class="skills__group">
          <div class="skills__h">Sviluppo &amp; programmazione</div>
          <div class="tags">
            <span class="tag">Python</span>
            <span class="tag">JavaScript</span>
            <span class="tag">HTML &amp; CSS</span>
            <span class="tag">PHP</span>
            <span class="tag">SQL</span>
          </div>
        </div>
        <div class="skills__group">
          <div class="skills__h">Reti &amp; sistemi</div>
          <div class="tags">
            <span class="tag">Subnetting / VLSM</span>
            <span class="tag">VLAN</span>
            <span class="tag">Routing</span>
            <span class="tag">Firewall &amp; DMZ</span>
            <span class="tag">Linux</span>
          </div>
        </div>
        <div class="skills__group">
          <div class="skills__h">Strumenti &amp; metodo</div>
          <div class="tags">
            <span class="tag">Git</span>
            <span class="tag">API REST</span>
            <span class="tag">Database relazionali</span>
            <span class="tag">Progettazione UI</span>
          </div>
        </div>
      </div>
    </div>

    <div class="editorial reveal">
      <div class="editorial__label">Oltre la scuola</div>
      <div class="prose">
        <p>
          Fuori dall'aula mi trovi a sperimentare con il <strong>web design</strong>, a
          seguire progetti imprenditoriali e a coltivare qualche passione meno tecnica —
          dalle auto al mondo della moda. Curiosità che, in un modo o nell'altro, finiscono
          sempre per influenzare il modo in cui costruisco.
        </p>
        <p>
          Cosa c'è dopo? Continuare a imparare, possibilmente costruendo. Mi interessa unire
          competenze tecniche e visione imprenditoriale: questo portfolio non è un punto di
          arrivo, ma <span class="accent">il punto di partenza</span>.
        </p>
      </div>
    </div>
  </div>
</section>

<!-- ──────────────────────── CTA BAND ──────────────────────── -->
<section class="section section--tight section--panel">
  <div class="container cta-band reveal">
    <span class="eyebrow" style="justify-content:center">Continua a esplorare</span>
    <h2 class="cta-band__title">Il percorso non finisce qui.</h2>
    <div class="cta-band__row">
      <a class="btn btn--primary" href="{base}/educazione-civica">Educazione civica <span class="arrow">→</span></a>
      <a class="btn btn--ghost" href="{base}/">Torna alla home</a>
    </div>
  </div>
</section>