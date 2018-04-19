<template>
  <div class="row">
    <app-quote-item v-for="quote in quotes" :key="quote" :quote="quote"></app-quote-item>
  </div>
</template>

<script>
  export default {
    props: {
      quotes: Array
    }
  }
</script>
