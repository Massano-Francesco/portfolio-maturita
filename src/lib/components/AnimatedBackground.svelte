<script>
  export let variant = 'default'; // 'default' | 'hero' | 'dark'
</script>

<div class="animated-bg variant-{variant}">
  <div class="orb orb-1"></div>
  <div class="orb orb-2"></div>
  <div class="orb orb-3"></div>

  <div class="particles">
    {#each Array(20) as _, i}
      <div
        class="particle"
        style="
          left: {Math.random() * 100}%;
          top: {Math.random() * 100}%;
          animation-delay: {Math.random() * 6}s;
          animation-duration: {4 + Math.random() * 8}s;
          width: {1 + Math.random() * 2}px;
          height: {1 + Math.random() * 2}px;
          opacity: {0.2 + Math.random() * 0.5};
        "
      ></div>
    {/each}
  </div>

  <div class="scanline"></div>
</div>

<style>
  .animated-bg {
    position: absolute;
    inset: 0;
    overflow: hidden;
    pointer-events: none;
  }

  .orb {
    position: absolute;
    border-radius: 50%;
    filter: blur(80px);
    animation: orbFloat 12s ease-in-out infinite;
  }

  .orb-1 {
    width: 500px; height: 500px;
    background: radial-gradient(circle, rgba(34, 211, 238, 0.1) 0%, transparent 70%);
    top: -100px; right: -100px;
    animation-delay: 0s;
  }

  .orb-2 {
    width: 400px; height: 400px;
    background: radial-gradient(circle, rgba(52, 211, 153, 0.12) 0%, transparent 70%);
    bottom: -80px; left: -80px;
    animation-delay: -4s;
  }

  .orb-3 {
    width: 300px; height: 300px;
    background: radial-gradient(circle, rgba(251, 146, 60, 0.08) 0%, transparent 70%);
    top: 40%; left: 40%;
    animation-delay: -8s;
  }

  .variant-hero .orb-1 { opacity: 1.5; width: 700px; height: 700px; }
  .variant-dark .orb { opacity: 0.5; }

  @keyframes orbFloat {
    0%, 100% { transform: translate(0, 0) scale(1); }
    33% { transform: translate(30px, -20px) scale(1.05); }
    66% { transform: translate(-20px, 30px) scale(0.95); }
  }

  .particles {
    position: absolute;
    inset: 0;
  }

  .particle {
    position: absolute;
    background: var(--accent-cyan);
    border-radius: 50%;
    animation: particleFloat linear infinite;
    box-shadow: 0 0 4px var(--accent-cyan);
  }

  @keyframes particleFloat {
    0% { transform: translateY(0) translateX(0); opacity: 0; }
    10% { opacity: 1; }
    90% { opacity: 1; }
    100% { transform: translateY(-100vh) translateX(30px); opacity: 0; }
  }

  .scanline {
    position: absolute;
    left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, transparent, rgba(34, 211, 238, 0.08), transparent);
    animation: scanline 8s linear infinite;
    pointer-events: none;
  }

  @keyframes scanline {
    from { top: -2px; }
    to { top: 100%; }
  }
</style>
