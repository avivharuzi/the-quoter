<template>
  <div class="container">
    <app-header></app-header>
    <app-quote-form @newQuote="onNewQuote"></app-quote-form>
    <app-quote-list :quotes="quotes"></app-quote-list>
  </div>
</template>

<script>
  import Header from '@/components/shared/Header'
  import QuoteForm from '@/components/Quote/QuoteForm'
  import QuoteList from '@/components/Quote/QuoteList'

  export default {
    data () {
      return {
        quotes: [],
        maxQuotes: 10
      }
    },
    methods: {
      onNewQuote (newQuote) {
        this.quotes.push(newQuote);
      }
    },
    components: {
      'app-header': Header,
      'app-quote-form': QuoteForm,
      'app-quote-list': QuoteList
    }
  }
</script>
