<script lang="ts">
export default {
  props: ['contributors'],
  frontMatter: {
    title: 'A tragic tale',
    layout: 'layout.njk'
  }
}

</script>
<template>
  <article>
    <h2>{{ title }}</h2>
    <p>Did YOU ever hear the Tragedy of Darth Plagueis the Wise?</p>
    <ul>
      <li v-for="contributor in contributors" :key="contributor.ghProfile">
        <a href="{{ contributor.ghProfile }}">{{ contributor.name }}</a>
      </li>
    </ul>
  </article>
</template>