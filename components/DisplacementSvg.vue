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
      <filter
        id="turbulence--animated"
        x="-10%"
        y="-20%"
        width="120%"
        height="140%"
      >
        <feTurbulence
          type="fractalNoise"
          baseFrequency="0.002"
          result="fracNoise"
        />
        <feColorMatrix type="hueRotate" values="180">
          <animate
            attributeName="values"
            from="0"
            to="360"
            dur="10s"
            repeatCount="indefinite"
          />
        </feColorMatrix>
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
<script>
export default {
  data() {
    return {}
  }
}
</script>
