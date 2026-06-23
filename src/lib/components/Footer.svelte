<script>
  const year = new Date().getFullYear();
</script>

<footer class="footer">
  <div class="footer-glow"></div>
  <div class="container">
    <div class="footer-inner">
      <div class="footer-brand">
        <span class="brand-logo">&lt;PM/&gt;</span>
        <p class="brand-tagline">Portfolio Digitale — F. E. Massano</p>
      </div>

      <div class="footer-quote">
        <p>"Il codice è il linguaggio con cui<br/>trasformiamo il pensiero in realtà."</p>
        <span class="quote-line"></span>
      </div>

      <div class="footer-social">
        <a href="mailto:francescoedoardo.massano@gmail.com" class="social-link" aria-label="Email">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
            <rect x="2" y="4" width="20" height="16" rx="2"/>
            <polyline points="2,4 12,13 22,4"/>
          </svg>
        </a>
        <a href="https://github.com/FrancescoEdoardoMassano" target="_blank" class="social-link" aria-label="GitHub">
          <svg viewBox="0 0 24 24" fill="currentColor">
            <path d="M12 2C6.477 2 2 6.477 2 12c0 4.42 2.87 8.17 6.84 9.5.5.08.66-.23.66-.5v-1.69c-2.77.6-3.36-1.34-3.36-1.34-.46-1.16-1.11-1.47-1.11-1.47-.91-.62.07-.6.07-.6 1 .07 1.53 1.03 1.53 1.03.87 1.52 2.34 1.07 2.91.83.09-.65.35-1.09.63-1.34-2.22-.25-4.55-1.11-4.55-4.92 0-1.11.38-2 1.03-2.71-.1-.25-.45-1.29.1-2.64 0 0 .84-.27 2.75 1.02.79-.22 1.65-.33 2.5-.33.85 0 1.71.11 2.5.33 1.91-1.29 2.75-1.02 2.75-1.02.55 1.35.2 2.39.1 2.64.65.71 1.03 1.6 1.03 2.71 0 3.82-2.34 4.66-4.57 4.91.36.31.69.92.69 1.85V21c0 .27.16.59.67.5C19.14 20.16 22 16.42 22 12A10 10 0 0012 2z"/>
          </svg>
        </a>
        <a href="https://linkedin.com" target="_blank" class="social-link" aria-label="LinkedIn">
          <svg viewBox="0 0 24 24" fill="currentColor">
            <path d="M16 8a6 6 0 016 6v7h-4v-7a2 2 0 00-2-2 2 2 0 00-2 2v7h-4v-7a6 6 0 016-6zM2 9h4v12H2z"/>
            <circle cx="4" cy="4" r="2"/>
          </svg>
        </a>
      </div>
    </div>

    <div class="footer-bottom">
      <span class="mono" style="color: var(--text-muted); font-size: 0.75rem;">
        © {year} — Portfolio Digitale — Maturità 2026
      </span>
      <!-- <span class="footer-status">
        <span class="status-dot"></span>
        <span class="mono" style="font-size: 0.7rem; color: var(--text-muted);">Sistema Online</span>
      </span> -->
    </div>
  </div>
</footer>

<style>
  .footer {
    position: relative;
    padding: 60px 0 32px;
    border-top: 1px solid var(--border-subtle);
    overflow: hidden;
  }

  .footer-glow {
    position: absolute;
    top: 0; left: 50%;
    transform: translateX(-50%);
    width: 600px; height: 1px;
    background: linear-gradient(90deg, transparent, var(--accent-cyan), var(--accent-violet), transparent);
    filter: blur(1px);
  }

  .container {
    max-width: 1280px;
    margin: 0 auto;
    padding: 0 32px;
  }

  .footer-inner {
    display: grid;
    grid-template-columns: 1fr auto 1fr;
    align-items: center;
    gap: 40px;
    margin-bottom: 48px;
  }

  .footer-brand { display: flex; flex-direction: column; gap: 8px; }

  .brand-logo {
    font-family: var(--font-display);
    font-size: 1.5rem;
    font-weight: 800;
    color: var(--accent-cyan);
    text-shadow: var(--glow-text);
  }

  .brand-tagline {
    font-family: var(--font-mono);
    font-size: 0.7rem;
    color: var(--text-muted);
    letter-spacing: 0.1em;
    text-transform: uppercase;
  }

  .footer-quote {
    text-align: center;
    position: relative;
    padding: 0 40px;
  }

  .footer-quote p {
    font-family: var(--font-display);
    font-size: 1rem;
    color: var(--text-secondary);
    line-height: 1.6;
    font-style: italic;
  }

  .quote-line {
    display: block;
    width: 40px; height: 1px;
    background: var(--accent-cyan);
    margin: 12px auto 0;
    box-shadow: 0 0 6px var(--accent-cyan);
  }

  .footer-social {
    display: flex;
    gap: 16px;
    justify-content: flex-end;
  }

  .social-link {
    width: 44px; height: 44px;
    border: 1px solid var(--border-subtle);
    border-radius: 8px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--text-muted);
    transition: all 0.25s;
  }

  .social-link svg { width: 18px; height: 18px; }

  .social-link:hover {
    border-color: var(--accent-cyan);
    color: var(--accent-cyan);
    box-shadow: 0 0 12px rgba(0, 212, 255, 0.3);
    transform: translateY(-2px);
  }

  .footer-bottom {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding-top: 24px;
    border-top: 1px solid var(--border-subtle);
  }

  .footer-status { display: flex; align-items: center; gap: 8px; }

  .status-dot {
    width: 6px; height: 6px;
    background: var(--accent-neon);
    border-radius: 50%;
    box-shadow: 0 0 8px var(--accent-neon);
    animation: pulse 2s ease-in-out infinite;
  }

  @keyframes pulse {
    0%, 100% { opacity: 1; transform: scale(1); }
    50% { opacity: 0.5; transform: scale(0.8); }
  }

  @media (max-width: 768px) {
    .footer-inner {
      grid-template-columns: 1fr;
      text-align: center;
    }
    .footer-social { justify-content: center; }
    .footer-quote { padding: 0; }
    .container { padding: 0 20px; }
  }
</style>
