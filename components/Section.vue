<template>
  <section class="section" data-emergence="hidden">
    <p
      v-for="(paragraph, index) of content"
      :key="index"
      class="section__content"
      v-html="paragraph"
    ></p>
  </section>
</template>

<script>
export default {
  props: {
    content: {
      type: Array,
      default: () => []
    }
  }
}
</script>
