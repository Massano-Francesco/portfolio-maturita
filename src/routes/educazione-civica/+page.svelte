<script>
  import { base } from "$app/paths";
  import AnimatedBackground from "$lib/components/AnimatedBackground.svelte";

  // ─── DATI PROGETTI ───────────────────────────────────────────────────────────
  // Per ogni progetto:
  //   previewSrc  → URL diretto a un'immagine (es. '/img/progetto1.jpg' nella cartella static/)
  //   embedUrl    → URL embed di Canva o Google Slides (vedi NOTE sotto)
  //   projectUrl  → link opzionale al progetto (es. GitHub, sito, PDF)
  //
  // NOTE EMBED:
  //   Canva   → Condividi → Incorpora → copia l'URL src dell'<iframe>
  //   G.Slide → File → Pubblica sul web → Incorpora → copia l'URL src dell'<iframe>
  // ─────────────────────────────────────────────────────────────────────────────

  const progetti = [
    {
      anno: "3",
      annoLabel: "Terzo Anno",
      items: [
        {
          id: "3-01",
          titolo: "Calcolatore di codice fiscale",
          materia: "Informatica",
          materiaColor: "#22d3ee",
          desc: "Un programma sviluppato in C capace di generare automaticamente il codice fiscale partendo dai dati anagrafici dell’utente.",
          punti: [
            "Strutture base del linguaggio C",
            "Gestione di stringhe e input utente",
            "Logica di calcolo del codice fiscale italiano",
          ],
          previewSrc: `${base}/img_antep/codice_fiscale.png`,
          embedUrl: null,
          projectUrl: "https://github.com/Massano-Francesco/codice_fiscale",
        },
        {
          id: "3-03",
          titolo: "La Mattanza",
          materia: "Storia",
          materiaColor: "#fb923c",
          desc: "Un progetto dedicato al fenomeno delle stragi mafiose e alla violenza utilizzata dalla criminalità organizzata durante gli anni più critici della lotta alla mafia.",
          punti: [
            "Le stragi mafiose in Italia",
            "Figure simbolo della lotta alla mafia",
            "Impatto sociale e politico della criminalità organizzata",
          ],
          previewSrc: `${base}/img_antep/mattanza.png`,
          embedUrl: null,
          projectUrl: null,
        },
      ],
    },
    {
      anno: "4",
      annoLabel: "Quarto Anno",
      items: [
        {
          id: "4-01",
          titolo: "Quiz Patente",
          materia: "Informatica",
          materiaColor: "#22d3ee",
          desc: "Un simulatore di quiz della patente sviluppato in Python con Tkinter, progettato per esercitarsi in modo realistico e interattivo.",
          punti: [
            "Interfacce grafiche con Tkinter",
            "Gestione di domande e punteggi",
            "Simulazione realistica dei quiz patente",
          ],
          previewSrc: `${base}/img_antep/quiz_patente.png`,
          embedUrl: null,
          projectUrl: "https://github.com/Massano-Francesco/QUIZ-PATENTE",
        },
        {
          id: "4-02",
          titolo: "I Pellerossa",
          materia: "Italiano & Storia",
          materiaColor: "#fb923c",
          desc: "Un’analisi dei nativi americani, delle loro origini storiche, delle tradizioni culturali e del loro impatto sulla storia e sulla società del continente americano.",
          punti: [
            "Origini e storia dei nativi americani",
            "Tradizioni, culture e organizzazione sociale",
            "Influenza storica e contributo culturale",
          ],
          previewSrc: `${base}/img_antep/pellerossa.png`,
          embedUrl:
            "https://www.canva.com/design/DAHNaQyaKhw/o61pdhoV1IcIbx9mEwRz9w/view?embed",
          projectUrl: null,
        },
        {
          id: "4-03",
          titolo: "Space Invaders",
          materia: "Informatica",
          materiaColor: "#22d3ee",
          desc: "Un clone del classico arcade game sviluppato in Python con Pygame: nemici, livelli progressivi, punteggio e vite.",
          punti: [
            "Game loop e gestione eventi con Pygame",
            "Collision detection e movimento dei nemici",
            "Sistema di punteggio, vite e livelli",
          ],
          previewSrc: `${base}/img_antep/space_invaders.png`,
          embedUrl: null,
          projectUrl: "https://github.com/Massano-Francesco/gioco_pygame",
        },
      ],
    },
    {
      anno: "5",
      annoLabel: "Quinto Anno",
      items: [
        {
          id: "5-01",
          titolo: "Lager",
          materia: "Storia",
          materiaColor: "#818cf8",
          desc: "Un percorso interdisciplinare dedicato ai lager nazisti, alla disumanizzazione e alla riflessione filosofica sulla perdita dei diritti umani.",
          punti: [
            "I campi di concentramento nazisti",
            "La negazione della dignità umana",
            "Memoria storica e riflessione etica",
          ],
          previewSrc: `${base}/img_antep/lager.png`,
          embedUrl:
            "https://www.canva.com/design/DAHJ9aEgIgw/2uBiUGDhyoxr03Mwe5km-A/view?embed",
          projectUrl: null,
        },
        {
          id: "5-02",
          titolo: "1522",
          materia: "Informatica",
          materiaColor: "#818cf8",
          desc: "Un progetto dedicato agli eventi storici e culturali del 1522, con riferimento ai cambiamenti politici, religiosi e sociali del XVI secolo.",
          punti: [
            "Contesto storico del Cinquecento",
            "Trasformazioni religiose e politiche",
            "Impatto culturale degli eventi del 1522",
          ],
          previewSrc: `${base}/img_antep/1522.png`,
          embedUrl: "",
          projectUrl: "https://github.com/Massano-Francesco/progetto_1522",
        },
        {
          id: "5-03",
          titolo: "Aktion T4 e progetto Lebensborn",
          materia: "Storia",
          materiaColor: "#34d399",
          desc: "Un approfondimento sui programmi eugenetici nazisti Aktion T4 e Lebensborn, simboli della propaganda razziale del Terzo Reich.",
          punti: [
            "Eugenetica e ideologia nazista",
            "Il programma Aktion T4",
            "Il progetto Lebensborn e la propaganda razziale",
          ],
          previewSrc: `${base}/img_antep/aktion_t4.png`,
          embedUrl:
            "https://www.canva.com/design/DAHJ9Syb6Pw/xS9OpptKBKzgCnwA4tTByA/view?embed",
          projectUrl: null,
        },
        {
          id: "5-04",
          titolo: "'68 e Costituzione",
          materia: "Storia e cultura generale",
          materiaColor: "#34d399",
          desc: "Un’analisi del Sessantotto italiano e dei cambiamenti sociali, politici e culturali collegati ai principi della Costituzione.",
          punti: [
            "Il movimento del Sessantotto",
            "Diritti civili e partecipazione politica",
            "Valori costituzionali e cambiamento sociale",
          ],
          previewSrc: `${base}/img_antep/sessantotto.png`,
          embedUrl:
            "https://www.canva.com/design/DAHJ_nsTC_I/WBnV7oHXu_0QbsKzRbBAVQ/view?embed",
          projectUrl: null,
        },
        {
          id: "5-05",
          titolo: "La prigione domestica",
          materia: "Cultura generale ed educazione civica",
          materiaColor: "#34d399",
          desc: "Un approfondimento sulla condizione femminile nella società italiana del Novecento, tra discriminazioni, emancipazione e tutela dei diritti sanciti dalla Costituzione.",
          punti: [
            "Ruolo della donna nella società",
            "Emancipazione femminile e diritti civili",
            "Uguaglianza e principi costituzionali",
          ],
          previewSrc: `${base}/img_antep/prigione_domestica.png`,
          embedUrl: `${base}/pdfs/La_prigione_domestica_Massano_e_Ardoino.pdf`,
          projectUrl: null,
        },
        {
          id: "5-06",
          titolo: "L'amore mio non muore - Roberto Saviano",
          materia: "Educazione civica e attualità",
          materiaColor: "#34d399",
          desc: "Un'analisi della violenza di genere e del fenomeno del femminicidio attraverso il racconto di Rossella Casini, simbolo di coraggio e di lotta contro la criminalità organizzata.",
          punti: [
            "Violenza di genere e femminicidio",
            "Il ruolo della criminalità organizzata",
            "Memoria, giustizia e impegno civile",
          ],
          previewSrc: `${base}/img_antep/saviano.png`,
          embedUrl: null,
          projectUrl: null,
        },
        {
          id: "5-07",
          titolo: "La zona grigia - Primo Levi",
          materia: "Storia ed educazione civica",
          materiaColor: "#34d399",
          desc: "Una riflessione sui dilemmi morali nei campi di concentramento e sulla complessità delle responsabilità individuali durante i regimi totalitari.",
          punti: [
            "La Shoah e i campi di concentramento",
            "Responsabilità e ambiguità morale",
            "Memoria storica e diritti umani",
          ],
          previewSrc: `${base}/img_antep/zona_grigia.png`,
          embedUrl: null,
          projectUrl: null,
        },
        {
          id: "5-08",
          titolo: "Social and ethical problems of Internet",
          materia: "Inglese ed educazione civica",
          materiaColor: "#34d399",
          desc: "An overview of the main social and ethical issues related to Internet use, including inequalities in access, threats to cultural diversity, and limitations on freedom of expression.",
          punti: [
            "Digital divide",
            "Erosion of cultural industries",
            "Censorship",
          ],
          previewSrc: `${base}/img_antep/social_internet.png`,
          embedUrl: null,
          projectUrl: null,
        },
        {
          id: "5-10",
          titolo: "Advantages and disadvantages of AI",
          materia: "Inglese ed educazione civica",
          materiaColor: "#34d399",
          desc: "Is AI advantageous for us or not?",
          punti: ["Occupation", "Reliability", "Losing crtical thinking"],
          previewSrc: `${base}/img_antep/ai_pros_cons.png`,
          embedUrl: null,
          projectUrl: null,
        },
        {
          id: "5-09",
          titolo: "Online dangers and how to use the Internet safely",
          materia: "Inglese ed educazione civica",
          materiaColor: "#34d399",
          desc: "A list of problems that the use of Internet lead to",
          punti: ["Malware", "Worm", "Firewall"],
          previewSrc: `${base}/img_antep/internet_safety.png`,
          embedUrl: null,
          projectUrl: null,
        },
      ],
    },
  ];

  const totalProgetti = progetti.reduce((n, g) => n + g.items.length, 0);

  let selectedProject = null;

  function openProject(p) {
    selectedProject = p;
  }
  function closeProject() {
    selectedProject = null;
  }
</script>

<svelte:head>
  <title>Educazione Civica — Francesco Edoardo Massano</title>
</svelte:head>

<!-- Hero -->
<section class="page-hero">
  <AnimatedBackground />
  <div class="hero-glow"></div>
  <div class="container hero-inner">
    <div class="section-label reveal">02 / Educazione Civica</div>
    <h1 class="reveal">
      Portfolio<br />
      <span class="gradient-text">Digitale</span>
    </h1>
    <p class="reveal">
      I temi trasversali che collegano tecnologia, società e responsabilità
      civile. Un percorso interdisciplinare tra informatica, diritto, storia e
      scienze.
    </p>
    <div class="hero-stats reveal">
      <div class="stat-pill">
        <span class="stat-num">{totalProgetti}</span>
        <span class="stat-label mono">Progetti</span>
      </div>
      <div class="stat-pill">
        <span class="stat-num">3</span>
        <span class="stat-label mono">Anni</span>
      </div>
      <div class="stat-pill">
        <span class="stat-num">6+</span>
        <span class="stat-label mono">Materie</span>
      </div>
    </div>
  </div>
</section>

<!-- Progetti per anno -->
{#each progetti as gruppo, gi}
  <section class="section anno-section" class:anno-alt={gi % 2 === 1}>
    <div class="container">
      <div class="anno-header reveal">
        <div class="anno-badge-wrap">
          <div class="anno-badge">{gruppo.anno}</div>
          <div class="anno-ring"></div>
        </div>
        <div class="anno-header-text">
          <div class="section-label">{gruppo.annoLabel}</div>
          <h2>
            Progetti del <span class="gradient-text">{gruppo.annoLabel}</span>
          </h2>
          <span class="anno-count mono"
            >{gruppo.items.length}
            {gruppo.items.length === 1 ? "progetto" : "progetti"}</span
          >
        </div>
        <div class="anno-line"></div>
      </div>

      <div class="progetti-grid">
        {#each gruppo.items as progetto, i}
          <div
            class="progetto-card glass-card reveal"
            style="--accent: {progetto.materiaColor}; animation-delay:{i *
              0.08}s"
            on:click={() => openProject(progetto)}
            role="button"
            tabindex="0"
            on:keydown={(e) => e.key === "Enter" && openProject(progetto)}
          >
            <!-- Anteprima -->
            <div class="progetto-preview">
              {#if progetto.previewSrc}
                <img
                  src={progetto.previewSrc}
                  alt="Anteprima {progetto.titolo}"
                  class="preview-img"
                  loading="lazy"
                />
                <div class="preview-overlay"></div>
              {:else}
                <div class="preview-placeholder">
                  <svg
                    viewBox="0 0 48 48"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <rect
                      x="4"
                      y="8"
                      width="40"
                      height="32"
                      rx="4"
                      stroke="currentColor"
                      stroke-width="1.5"
                    />
                    <path
                      d="M4 28l12-10 8 8 6-5 14 11"
                      stroke="currentColor"
                      stroke-width="1.5"
                      stroke-linejoin="round"
                    />
                    <circle
                      cx="16"
                      cy="18"
                      r="4"
                      stroke="currentColor"
                      stroke-width="1.5"
                    />
                  </svg>
                  <span class="mono">Anteprima</span>
                </div>
              {/if}
              <div class="preview-badges">
                <div
                  class="materia-badge"
                  style="background: {progetto.materiaColor}25; border-color: {progetto.materiaColor}50; color: {progetto.materiaColor}"
                >
                  {progetto.materia}
                </div>
                {#if progetto.embedUrl}
                  <div class="slide-badge">
                    <svg
                      viewBox="0 0 16 16"
                      fill="currentColor"
                      width="12"
                      height="12"
                      ><path
                        d="M2 2h12v10H2V2zm1 1v8h10V3H3zm2 1h6v1H5V4zm0 2h6v1H5V6zm0 2h4v1H5V8z"
                      /></svg
                    >
                    Presentazione
                  </div>
                {/if}
              </div>
              <div class="preview-hover-cta">
                <span>Visualizza →</span>
              </div>
            </div>

            <!-- Info -->
            <div class="progetto-info">
              <h3 class="progetto-titolo">{progetto.titolo}</h3>
              <p class="progetto-desc">{progetto.desc}</p>
              <div class="progetto-footer">
                <span class="view-link">Apri progetto →</span>
                {#if progetto.projectUrl}
                  <span class="github-dot" title="Link disponibile"></span>
                {/if}
              </div>
            </div>

            <div class="accent-bar"></div>
          </div>
        {/each}
      </div>
    </div>
  </section>
{/each}

<!-- Modal dettaglio -->
{#if selectedProject}
  <div
    class="modal-overlay"
    on:click={closeProject}
    role="dialog"
    aria-modal="true"
  >
    <div class="modal-panel glass-card" on:click|stopPropagation>
      <button
        class="modal-close btn-icon"
        on:click={closeProject}
        aria-label="Chiudi"
      >
        <svg
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2"
        >
          <path d="M18 6L6 18M6 6l12 12" />
        </svg>
      </button>

      <!-- Embed presentazione (Canva / Google Slides) -->
      {#if selectedProject.embedUrl}
        <div class="modal-embed">
          <iframe
            src={selectedProject.embedUrl}
            title="Presentazione {selectedProject.titolo}"
            frameborder="0"
            allowfullscreen
          ></iframe>
        </div>
      {:else if selectedProject.previewSrc}
        <div class="modal-preview-img-wrap">
          <img
            src={selectedProject.previewSrc}
            alt="Anteprima {selectedProject.titolo}"
          />
        </div>
      {:else}
        <div class="modal-preview-placeholder">
          <svg viewBox="0 0 64 64" fill="none">
            <rect
              x="4"
              y="8"
              width="56"
              height="48"
              rx="6"
              stroke="currentColor"
              stroke-width="1.5"
            />
            <path
              d="M4 40l18-14 10 10 8-7 20 16"
              stroke="currentColor"
              stroke-width="1.5"
              stroke-linejoin="round"
            />
            <circle
              cx="20"
              cy="22"
              r="6"
              stroke="currentColor"
              stroke-width="1.5"
            />
          </svg>
          <p class="mono">Presentazione non ancora disponibile</p>
        </div>
      {/if}

      <!-- Body -->
      <div class="modal-body">
        <div class="modal-meta">
          <span
            class="materia-badge-inline"
            style="background: {selectedProject.materiaColor}20; border-color: {selectedProject.materiaColor}40; color: {selectedProject.materiaColor}"
          >
            {selectedProject.materia}
          </span>
        </div>

        <h2 class="modal-title">{selectedProject.titolo}</h2>
        <p class="modal-desc">{selectedProject.desc}</p>

        <ul class="modal-punti">
          {#each selectedProject.punti as punto}
            <li>
              <span
                class="punto-dot"
                style="background:{selectedProject.materiaColor}; box-shadow: 0 0 6px {selectedProject.materiaColor}"
              ></span>
              {punto}
            </li>
          {/each}
        </ul>

        <!-- CTA buttons -->
        <div class="modal-actions">
          {#if selectedProject.embedUrl}
            <a
              href={selectedProject.embedUrl}
              target="_blank"
              rel="noopener"
              class="btn-solid"
            >
              Apri presentazione
              <svg
                viewBox="0 0 24 24"
                fill="none"
                stroke="currentColor"
                stroke-width="2"
                width="16"
                height="16"
                ><path
                  d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"
                /><polyline points="15 3 21 3 21 9" /><line
                  x1="10"
                  y1="14"
                  x2="21"
                  y2="3"
                /></svg
              >
            </a>
          {/if}
          {#if selectedProject.projectUrl}
            <a
              href={selectedProject.projectUrl}
              target="_blank"
              rel="noopener"
              class="btn-glow"
            >
              Vai al progetto →
            </a>
          {/if}
        </div>
      </div>
    </div>
  </div>
{/if}

<style>
  .page-hero {
    position: relative;
    min-height: 58vh;
    display: flex;
    align-items: flex-end;
    padding: calc(var(--navbar-h, 72px) + 60px) 0 80px;
    overflow: hidden;
    border-bottom: 1px solid var(--border-subtle);
  }

  .hero-glow {
    position: absolute;
    inset: 0;
    background: radial-gradient(
        ellipse at 30% 30%,
        rgba(34, 211, 238, 0.14),
        transparent 55%
      ),
      radial-gradient(
        ellipse at 70% 60%,
        rgba(52, 211, 153, 0.08),
        transparent 50%
      );
    pointer-events: none;
  }

  .hero-inner h1 {
    font-size: clamp(3rem, 7vw, 6rem);
    margin-bottom: 16px;
  }
  .hero-inner p {
    font-size: 1.05rem;
    color: var(--text-secondary);
    max-width: 560px;
    margin-bottom: 28px;
  }

  .hero-stats {
    display: flex;
    gap: 16px;
    flex-wrap: wrap;
  }

  .stat-pill {
    display: flex;
    flex-direction: column;
    gap: 2px;
    padding: 14px 22px;
    background: rgba(34, 211, 238, 0.06);
    border: 1px solid rgba(34, 211, 238, 0.2);
    border-radius: var(--radius-md);
    min-width: 90px;
  }

  .stat-num {
    font-family: var(--font-display);
    font-size: 1.6rem;
    font-weight: 800;
    color: var(--accent-cyan);
    line-height: 1;
  }

  .stat-label {
    font-size: 0.62rem;
    color: var(--text-muted);
    text-transform: uppercase;
    letter-spacing: 0.15em;
  }

  .anno-section {
    border-bottom: 1px solid var(--border-subtle);
    position: relative;
  }
  .anno-section:last-of-type {
    border-bottom: none;
  }
  .anno-alt {
    background: linear-gradient(
      180deg,
      rgba(34, 211, 238, 0.025) 0%,
      transparent 100%
    );
  }

  .anno-header {
    display: flex;
    align-items: flex-start;
    gap: 28px;
    margin-bottom: 52px;
    position: relative;
  }

  .anno-badge-wrap {
    position: relative;
    flex-shrink: 0;
  }

  .anno-badge {
    width: 72px;
    height: 72px;
    border-radius: 50%;
    background: linear-gradient(
      135deg,
      rgba(34, 211, 238, 0.15),
      rgba(52, 211, 153, 0.08)
    );
    border: 2px solid rgba(34, 211, 238, 0.35);
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: var(--font-display);
    font-size: 1.6rem;
    font-weight: 800;
    color: var(--accent-cyan);
    position: relative;
    z-index: 1;
  }

  .anno-ring {
    position: absolute;
    inset: -8px;
    border-radius: 50%;
    border: 1px solid rgba(34, 211, 238, 0.15);
    animation: ringSpin 12s linear infinite;
  }

  @keyframes ringSpin {
    from {
      transform: rotate(0deg);
    }
    to {
      transform: rotate(360deg);
    }
  }

  .anno-header-text {
    flex: 1;
  }
  .anno-header h2 {
    font-size: clamp(1.8rem, 3vw, 2.5rem);
    margin-bottom: 6px;
  }

  .anno-count {
    font-size: 0.68rem;
    color: var(--text-muted);
    text-transform: uppercase;
    letter-spacing: 0.12em;
  }

  .anno-line {
    position: absolute;
    bottom: -24px;
    left: 0;
    right: 0;
    height: 1px;
    background: linear-gradient(90deg, var(--accent-cyan), transparent 70%);
    opacity: 0.3;
  }

  .progetti-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 24px;
  }

  .progetto-card {
    display: flex;
    flex-direction: column;
    overflow: hidden;
    cursor: pointer;
    transition: all 0.35s cubic-bezier(0.4, 0, 0.2, 1);
    position: relative;
    --accent: var(--accent-cyan);
  }

  .progetto-card:hover {
    transform: translateY(-8px);
    border-color: color-mix(in srgb, var(--accent) 40%, transparent);
    box-shadow:
      0 24px 60px rgba(0, 0, 0, 0.45),
      0 0 40px color-mix(in srgb, var(--accent) 12%, transparent);
  }

  .progetto-preview {
    width: 100%;
    height: 220px;
    position: relative;
    overflow: hidden;
    background: rgba(34, 211, 238, 0.04);
    border-bottom: 1px solid var(--border-subtle);
  }

  .preview-img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: center top;
    transition: transform 0.5s cubic-bezier(0.4, 0, 0.2, 1);
  }

  .progetto-card:hover .preview-img {
    transform: scale(1.06);
  }

  .preview-overlay {
    position: absolute;
    inset: 0;
    background: linear-gradient(
      180deg,
      rgba(5, 3, 15, 0.1) 0%,
      rgba(5, 3, 15, 0) 40%,
      rgba(5, 3, 15, 0.75) 100%
    );
    pointer-events: none;
  }

  .preview-badges {
    position: absolute;
    top: 12px;
    left: 12px;
    right: 12px;
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    gap: 8px;
    z-index: 2;
  }

  .preview-hover-cta {
    position: absolute;
    bottom: 14px;
    left: 50%;
    transform: translateX(-50%) translateY(8px);
    opacity: 0;
    transition: all 0.3s ease;
    z-index: 2;
    padding: 6px 16px;
    background: rgba(5, 3, 15, 0.7);
    border: 1px solid color-mix(in srgb, var(--accent) 50%, transparent);
    border-radius: 100px;
    font-family: var(--font-mono);
    font-size: 0.68rem;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    color: var(--accent);
    backdrop-filter: blur(8px);
    white-space: nowrap;
  }

  .progetto-card:hover .preview-hover-cta {
    opacity: 1;
    transform: translateX(-50%) translateY(0);
  }

  .preview-placeholder {
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 12px;
    color: var(--text-muted);
  }

  .preview-placeholder svg {
    width: 48px;
    height: 48px;
    opacity: 0.4;
  }
  .preview-placeholder span {
    font-size: 0.65rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    opacity: 0.4;
  }

  .materia-badge {
    padding: 5px 11px;
    border-radius: 100px;
    border: 1px solid;
    font-family: var(--font-mono);
    font-size: 0.6rem;
    text-transform: uppercase;
    letter-spacing: 0.08em;
    font-weight: 600;
    backdrop-filter: blur(8px);
    max-width: 65%;
    line-height: 1.3;
  }

  .slide-badge {
    padding: 5px 11px;
    border-radius: 100px;
    background: rgba(5, 3, 15, 0.65);
    border: 1px solid rgba(34, 211, 238, 0.45);
    color: var(--accent-cyan);
    font-family: var(--font-mono);
    font-size: 0.6rem;
    text-transform: uppercase;
    letter-spacing: 0.08em;
    display: flex;
    align-items: center;
    gap: 4px;
    backdrop-filter: blur(8px);
    flex-shrink: 0;
  }

  .progetto-info {
    padding: 22px 24px 24px;
    display: flex;
    flex-direction: column;
    gap: 10px;
    flex: 1;
  }

  .progetto-titolo {
    font-size: 1rem;
    line-height: 1.35;
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
    overflow: hidden;
  }

  .progetto-desc {
    font-size: 0.82rem;
    color: var(--text-muted);
    line-height: 1.65;
    display: -webkit-box;
    -webkit-line-clamp: 3;
    -webkit-box-orient: vertical;
    overflow: hidden;
  }

  .progetto-footer {
    margin-top: auto;
    padding-top: 14px;
    border-top: 1px solid var(--border-subtle);
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .view-link {
    font-family: var(--font-mono);
    font-size: 0.72rem;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    color: var(--accent);
  }

  .github-dot {
    width: 8px;
    height: 8px;
    border-radius: 50%;
    background: var(--accent);
    box-shadow: 0 0 8px var(--accent);
    flex-shrink: 0;
  }

  .accent-bar {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    height: 3px;
    background: linear-gradient(
      90deg,
      var(--accent),
      color-mix(in srgb, var(--accent) 30%, transparent)
    );
    opacity: 0;
    transition: opacity 0.3s;
  }

  .progetto-card:hover .accent-bar {
    opacity: 1;
  }

  .modal-overlay {
    position: fixed;
    inset: 0;
    background: rgba(2, 4, 8, 0.88);
    backdrop-filter: blur(12px);
    z-index: 2000;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 20px;
    animation: fadeIn 0.2s ease;
  }

  @keyframes fadeIn {
    from {
      opacity: 0;
    }
    to {
      opacity: 1;
    }
  }

  .modal-panel {
    width: 100%;
    max-width: 900px;
    max-height: 90vh;
    overflow-y: auto;
    display: flex;
    flex-direction: column;
    position: relative;
    animation: slideUp 0.35s cubic-bezier(0.34, 1.56, 0.64, 1);
    /* sfondo PIENO e opaco → netto contrasto col contenuto */
    background: #0b0f1a !important;
    border: 1px solid rgba(34, 211, 238, 0.4) !important;
    border-radius: 18px;
    box-shadow:
      0 30px 90px rgba(0, 0, 0, 0.7),
      0 0 60px rgba(34, 211, 238, 0.1);
  }

  @keyframes slideUp {
    from {
      opacity: 0;
      transform: translateY(30px) scale(0.98);
    }
    to {
      opacity: 1;
      transform: translateY(0) scale(1);
    }
  }

  .btn-icon {
    position: absolute;
    top: 16px;
    right: 16px;
    width: 38px;
    height: 38px;
    background: rgba(5, 3, 15, 0.75);
    border: 1px solid var(--border-subtle);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--text-muted);
    z-index: 10;
    transition: all 0.2s;
    backdrop-filter: blur(8px);
  }

  .btn-icon:hover {
    background: rgba(34, 211, 238, 0.15);
    color: var(--text-primary);
    border-color: var(--border-glow);
  }

  .btn-icon svg {
    width: 16px;
    height: 16px;
  }

  .modal-embed {
    width: 100%;
    aspect-ratio: 16/9;
    background: #000;
    flex-shrink: 0;
    border-bottom: 1px solid var(--border-subtle);
  }

  .modal-embed iframe {
    width: 100%;
    height: 100%;
    border: none;
    display: block;
  }

  .modal-preview-img-wrap {
    width: 100%;
    max-height: 380px;
    overflow: hidden;
    border-bottom: 1px solid var(--border-subtle);
    flex-shrink: 0;
    background: #05030f;
  }

  .modal-preview-img-wrap img {
    width: 100%;
    height: 100%;
    object-fit: contain;
    display: block;
    max-height: 380px;
  }

  /* Placeholder modal */
  .modal-preview-placeholder {
    width: 100%;
    height: 220px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 16px;
    color: var(--text-muted);
    background: rgba(34, 211, 238, 0.02);
    border-bottom: 1px solid var(--border-subtle);
  }

  .modal-preview-placeholder svg {
    width: 64px;
    height: 64px;
    opacity: 0.3;
  }
  .modal-preview-placeholder p {
    font-size: 0.72rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    opacity: 0.4;
  }

  .modal-body {
    padding: 32px 36px;
    display: flex;
    flex-direction: column;
    gap: 20px;
  }

  .modal-meta {
    display: flex;
    gap: 10px;
    flex-wrap: wrap;
  }

  .materia-badge-inline {
    display: inline-flex;
    align-items: center;
    padding: 5px 14px;
    border-radius: 100px;
    border: 1px solid;
    font-family: var(--font-mono);
    font-size: 0.65rem;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    font-weight: 600;
  }

  .modal-title {
    font-size: 1.65rem;
    line-height: 1.25;
    color: #f1f5f9 !important;
  }

  .modal-desc {
    font-size: 0.92rem;
    color: #cbd5e1 !important;
    line-height: 1.75;
  }

  .modal-punti {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 10px;
    padding: 18px 20px;
    background: rgba(255, 255, 255, 0.04);
    border: 1px solid rgba(255, 255, 255, 0.12);
    border-radius: var(--radius-sm);
  }

  .modal-punti li {
    display: flex;
    align-items: flex-start;
    gap: 12px;
    font-size: 0.88rem;
    color: #e2e8f0 !important;
    line-height: 1.5;
  }

  .punto-dot {
    width: 6px;
    height: 6px;
    border-radius: 50%;
    flex-shrink: 0;
    margin-top: 7px;
  }

  .modal-actions {
    display: flex;
    gap: 14px;
    flex-wrap: wrap;
    padding-top: 4px;
  }

  /* Pulsanti del modal ben visibili sullo sfondo scuro */
  .modal-actions .btn-solid,
  .modal-actions .btn-glow {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 12px 22px;
    border-radius: 100px;
    font-family: var(--font-mono);
    font-size: 0.78rem;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.08em;
    text-decoration: none;
    transition: all 0.2s ease;
  }

  .modal-actions .btn-solid {
    background: #22d3ee !important;
    color: #04121a !important;
    border: 1px solid #22d3ee !important;
  }
  .modal-actions .btn-solid:hover {
    background: #67e8f9 !important;
    border-color: #67e8f9 !important;
    transform: translateY(-2px);
  }

  .modal-actions .btn-glow {
    background: rgba(34, 211, 238, 0.14) !important;
    color: #67e8f9 !important;
    border: 1px solid rgba(34, 211, 238, 0.6) !important;
  }
  .modal-actions .btn-glow:hover {
    background: rgba(34, 211, 238, 0.24) !important;
    border-color: #22d3ee !important;
    transform: translateY(-2px);
  }

  @media (max-width: 1100px) {
    .progetti-grid {
      grid-template-columns: repeat(2, 1fr);
    }
  }

  @media (max-width: 900px) {
    .anno-header {
      flex-direction: column;
      gap: 16px;
    }
    .anno-line {
      display: none;
    }
  }

  @media (max-width: 640px) {
    .progetti-grid {
      grid-template-columns: 1fr;
    }
    .progetto-preview {
      height: 200px;
    }
    .modal-panel {
      max-height: 95vh;
    }
    .modal-body {
      padding: 20px;
    }
    .modal-embed {
      aspect-ratio: 4/3;
    }
    .hero-stats {
      gap: 10px;
    }
    .stat-pill {
      padding: 10px 16px;
      min-width: 72px;
    }
    .stat-num {
      font-size: 1.3rem;
    }
  }
</style>