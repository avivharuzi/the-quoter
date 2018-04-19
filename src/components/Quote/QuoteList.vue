<template>
  <div class="row">
    <app-quote-item v-for="quote in quotes" :key="quote">{{ quote }}</app-quote-item>
  </div>
</template>

<script>
  import QuoteItem from '@/components/Quote/QuoteItem'

  export default {
    props: {
      quotes: Array
    },
    components: {
      'app-quote-item': QuoteItem
    }
  }
</script>
