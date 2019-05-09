<template>
  <div class="sections container">
    <Section
      :content="[`Hi, I’m <span class='is-outlined'>Henry Desroches.</span>`]"
    />
    <Section
      :content="[
        `I’m a creative developer from Denver with a passion for CSS, animation, accessibility, and deleting code.`
      ]"
    />
    <Section
      :content="[
        `I’ve worked on projects ranging from music e-commerce shops, large scale end-to-end mortgage fullfilment <a href='https://promontech.com'>app ecosystems</a>, and <a href='https://divinegoddessjessica.com'>dominatrix websites</a>.`
      ]"
    />
    <Section
      :content="[
        `I’ve been in interaction- and CSS-focused UI development jobs since 2015, most recently working at <a href='https://promontech.com' >Promontech</a> and <a href='https://universalmind.com'>Universal Mind</a>. I’m always open to new opportunities in creative dev or style-code-centric roles.`
      ]"
    />
    <Section
      :content="[
        `I’ve also open-sourced a bunch of code, such as <a href='https://super.henry.codes/'>an Alfred app</a> that makes your text much, much ˢᵐᵃˡˡᵉʳ ᵃⁿᵈ ʰᵃʳᵈᵉʳ ᵗᵒ ʳᵉᵃᵈ or a <a href='https://github.com/xdesro/threejs-webpack-starter'>simple Webpack/ThreeJS boilerplate</a>.`
      ]"
    />
    <Section
      :content="[
        `I’m most active and reachable <a href='https://twitter.com/xdesro'>on Twitter</a> or <a href='mailto:yo@henry.codes'>via email</a>,
    but you can find me most places on the internet as @xdesro.`
      ]"
    />
    <section class="section section--icons" data-emergence="hidden">
      <ul class="icons-list">
        <li
          v-for="(socialLink, index) of socialLinks"
          :key="index"
          class="icons-list__item"
        >
          <a class="icons-list__link" :href="socialLink.url">
            <Icon :icon="socialLink.name" class="icons-list__icon" />
          </a>
        </li>
      </ul>
    </section>
    <DisplacementSvg />
  </div>
</template>

<script>
import Section from '~/components/Section'
import Icon from '~/components/Icon'
import DisplacementSvg from '~/components/DisplacementSvg'
import emergence from 'emergence.js'

export default {
  components: {
    Section,
    Icon,
    DisplacementSvg
  },
  data() {
    return {
      socialLinks: [
        { name: 'twitter', url: 'https://twitter.com/xdesro' },
        { name: 'codepen', url: 'https://codepen.io/xdesro' },
        { name: 'github', url: 'https://github.com/xdesro' },
        { name: 'instagram', url: 'https://instagram.com/xdesro' },
        { name: 'twitch', url: 'https://twitch.tv/xdesro' },
        {
          name: 'stackoverflow',
          url: 'https://stackoverflow.com/users/7868234/henry-desroches'
        },
        { name: 'linkedin', url: 'https://www.linkedin.com/in/henrydesroches' }
      ]
    }
  },
  mounted() {
    emergence.init({
      reset: false
    })
  }
}
</script>
