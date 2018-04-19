<template>
  <div class="container">
    <app-header></app-header>
    <app-quote-list :quotes="quotes"></app-quote-list>
  </div>
</template>

<script>
  import Header from '@/components/shared/Header'
  import QuoteList from '@/components/Quote/QuoteList'

  export default {
    data () {
      return {
        quotes: [],
        maxQuotes: 10
      }
    },
    components: {
      'app-quote-list': QuoteList,
      'app-header': Header
    }
  }
</script>
