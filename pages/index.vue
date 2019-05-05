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
        <!-- <li class="icons-list__item" v-for="(socialLink, index) of socialLinks" :key="index">
          <a class="icons-list__link" :href="socialLink.url">

          </a>
        </li> -->
        <li class="icons-list__item">
          <a class="icons-list__link" href="https://twitter.com/xdesro">
            <IconTwitter class="icons-list__icon" />
          </a>
        </li>
        <li class="icons-list__item">
          <a class="icons-list__link" href="https://codepen.io/xdesro">
            <IconCodepen class="icons-list__icon" />
          </a>
        </li>
        <li class="icons-list__item">
          <a class="icons-list__link" href="https://github.com/xdesro/">
            <IconGithub class="icons-list__icon" />
          </a>
        </li>
        <li class="icons-list__item">
          <a class="icons-list__link" href="https://instagram.com/xdesro/">
            <IconInstagram class="icons-list__icon" />
          </a>
        </li>
        <li class="icons-list__item">
          <a class="icons-list__link" href="https://twitch.tv/xdesro/">
            <IconTwitch class="icons-list__icon" />
          </a>
        </li>
        <li class="icons-list__item">
          <a
            class="icons-list__link"
            href="https://stackoverflow.com/users/7868234/henry-desroches"
          >
            <IconStackoverflow class="icons-list__icon" />
          </a>
        </li>
        <li class="icons-list__item">
          <a
            class="icons-list__link"
            href="https://www.linkedin.com/in/henrydesroches"
          >
            <IconLinkedin class="icons-list__icon" />
          </a>
        </li>
      </ul>
    </section>
  </div>
</template>

<script>
import Section from '~/components/section'
import IconTwitter from '~/components/icons/IconTwitter'
import IconCodepen from '~/components/icons/IconCodepen'
import IconGithub from '~/components/icons/IconGithub'
import IconInstagram from '~/components/icons/IconInstagram'
import IconTwitch from '~/components/icons/IconTwitch'
import IconStackoverflow from '~/components/icons/IconStackoverflow'
import IconLinkedin from '~/components/icons/IconLinkedin'

export default {
  components: {
    Section,
    IconTwitter,
    IconCodepen,
    IconGithub,
    IconInstagram,
    IconTwitch,
    IconStackoverflow,
    IconLinkedin
  },
  data() {
    return {
      socialLinks: [
        { link: 'Twitter', url: 'https://google.com' },
        { link: 'Codepen', url: 'https://google.com' },
        { link: 'Github', url: 'https://google.com' },
        { link: 'Instagram', url: 'https://google.com' },
        { link: 'Twitch', url: 'https://google.com' },
        { link: 'Stackoverflow', url: 'https://google.com' },
        { link: 'Linkedin', url: 'https://google.com' }
      ]
    }
  }
}
</script>
