<script>
  import { base } from '$app/paths';
  const year = new Date().getFullYear();
</script>

<footer class="footer">
  <div class="container">
    <div class="footer__inner">
      <div>
        <div class="footer__brand">Francesco Edoardo Massano<span class="brand__dot">.</span></div>
        <p class="footer__tag">
          Portfolio digitale realizzato per l'Esame di Stato — un percorso di cinque anni
          in Informatica e Telecomunicazioni, raccontato con i fatti.
        </p>
      </div>

      <nav class="footer__nav" aria-label="Sezioni">
        <span class="footer__navlabel">Sezioni</span>
        <a class="footer__link" href="{base}/">Home</a>
        <a class="footer__link" href="{base}/chi-sono">Chi sono</a>
        <a class="footer__link" href="{base}/educazione-civica">Educazione civica</a>
      </nav>
    </div>

    <div class="footer__meta">
      <span>ITIS Edoardo Agnelli · Torino · A.S. 2025/26</span>
      <span>© {year} — F. E. Massano</span>
    </div>
  </div>
</footer>