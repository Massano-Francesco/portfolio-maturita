<script>
  // Kept the `variant` prop for API compatibility with existing usage.
  export let variant = 'hero';
</script>

<!-- Soft ambient glow -->
<div class="hero__glow" aria-hidden="true"></div>

<!-- Signature: telecom network — nodes, links and travelling signal -->
<svg class="hero__net" viewBox="0 0 520 520" fill="none" aria-hidden="true" data-variant={variant}>
  <!-- links -->
  <g class="signal-line">
    <line x1="90"  y1="120" x2="250" y2="70" />
    <line x1="250" y1="70"  x2="420" y2="140" />
    <line x1="90"  y1="120" x2="160" y2="260" />
    <line x1="250" y1="70"  x2="160" y2="260" />
    <line x1="250" y1="70"  x2="340" y2="280" />
    <line x1="420" y1="140" x2="340" y2="280" />
    <line x1="160" y1="260" x2="340" y2="280" />
    <line x1="160" y1="260" x2="90"  y2="400" />
    <line x1="340" y1="280" x2="430" y2="400" />
    <line x1="90"  y1="400" x2="250" y2="440" />
    <line x1="340" y1="280" x2="250" y2="440" />
    <line x1="250" y1="440" x2="430" y2="400" />
  </g>

  <!-- rings on hub nodes -->
  <circle class="signal-ring" cx="250" cy="70"  r="13" />
  <circle class="signal-ring" cx="340" cy="280" r="13" />

  <!-- nodes -->
  <g class="signal-node">
    <circle cx="90"  cy="120" r="4.5" />
    <circle cx="250" cy="70"  r="5.5" />
    <circle cx="420" cy="140" r="4.5" />
    <circle cx="160" cy="260" r="4.5" />
    <circle cx="340" cy="280" r="5.5" />
    <circle cx="90"  cy="400" r="4.5" />
    <circle cx="430" cy="400" r="4.5" />
    <circle cx="250" cy="440" r="4.5" />
  </g>

  <!-- travelling signals -->
  <circle r="3.5" class="signal-node">
    <animateMotion dur="4.6s" repeatCount="indefinite" path="M90,120 L250,70 L420,140 L340,280" />
    <animate attributeName="opacity" values="0;1;1;0" dur="4.6s" repeatCount="indefinite" />
  </circle>
  <circle r="3.5" class="signal-node">
    <animateMotion dur="5.4s" begin="1.2s" repeatCount="indefinite" path="M160,260 L340,280 L430,400 L250,440" />
    <animate attributeName="opacity" values="0;1;1;0" dur="5.4s" begin="1.2s" repeatCount="indefinite" />
  </circle>
</svg>