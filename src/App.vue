<template>
  <div class="container">
    <app-quote-list :quotes="quotes"></app-quote-list>
  </div>
</template>

<script>
  import QuoteList from '@/components/Quote/QuoteList'

  export default {
    data () {
      return {
        quotes: [],
        maxQuotes: 10
      }
    },
    components: {
      'app-quote-list': QuoteList
    }
  }
</script>
