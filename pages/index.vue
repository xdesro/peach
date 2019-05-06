<template>
  <div class="sections">
    <Section
      :content="[
        `Hi, I’m Henry Desroches.`,
        `I’m a creative developer from Denver with a passion for CSS, animation, accessibility, and deleting code.`
      ]"
    />
    <Section
      :content="[
        `I’ve worked on projects ranging from music e-commerce
    shops, large scale end-to-end mortgage fullfilment app ecosystems, and
    dominatrix websites.`
      ]"
    />
    <Section
      :content="[
        `I’ve been in interaction- and CSS-focused UI
    development jobs since 2015, most recently working at Promontech and
    Universal Mind. I’m always open to new opportunities in creative dev or
    style-code-centric roles.`
      ]"
    />
    <Section
      :content="[
        `I’ve written articles about <a href='#'>SVG techniques and animation</a>, VueJS, and advanced Sass and style code architecture. I’ve also open-sourced a bunch of code, such as an Alfred app that makes your text much, much ˢᵐᵃˡˡᵉʳ ᵃⁿᵈ ʰᵃʳᵈᵉʳ ᵗᵒ ʳᵉᵃᵈ or a simple Webpack/ThreeJS boilerplate.`
      ]"
    />
    <Section
      :content="[
        `I’m most active and reachable on Twitter or via email,
    but you can find me most places on the internet as @xdesro.`
      ]"
    />
    <section class="section section--icons">
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
  </div>
</template>

<script>
import Section from '~/components/section'
import Icon from '~/components/Icon'

export default {
  components: {
    Section,
    Icon
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
  }
}
</script>
