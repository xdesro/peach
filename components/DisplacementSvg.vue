<template>
  <svg class="displacement-map">
    <defs>
      <filter id="turbulence" x="-10%" y="0%" width="120%" height="100%">
        <feTurbulence
          type="fractalNoise"
          baseFrequency="0.002"
          result="fracNoise"
        />
        <feDisplacementMap
          in="SourceGraphic"
          in2="blurredFracNoise"
          scale="50"
          xChannelSelector="R"
          yChannelSelector="G"
        />
      </filter>
    </defs>
  </svg>
</template>
