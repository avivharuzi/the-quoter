<template>
  <div class="container">
    <app-header></app-header>
    <app-quote-form @newQuote="onNewQuote"></app-quote-form>
    <app-quote-list :quotes="quotes" @deletedQuote="onDeletedQuote"></app-quote-list>
    <app-quote-info></app-quote-info>
  </div>
</template>

<script>
  import Header from '@/components/shared/Header'
  import QuoteForm from '@/components/Quote/QuoteForm'
  import QuoteList from '@/components/Quote/QuoteList'
  import QuoteInfo from '@/components/Quote/QuoteInfo'

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
      },
      onDeletedQuote(deletedQuote) {
        this.quotes.splice(deletedQuote, 1)
      }
    },
    components: {
      'app-header': Header,
      'app-quote-form': QuoteForm,
      'app-quote-list': QuoteList,
      'app-quote-info': QuoteInfo
    }
  }
</script>
