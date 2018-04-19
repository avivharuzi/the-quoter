<template>
  <div class="container">
    <app-header></app-header>
    <app-quote-progress :quoteCount="quotes.length" :maxQuotes="maxQuotes"></app-quote-progress>
    <app-quote-form @newQuote="onNewQuote"></app-quote-form>
    <app-quote-list :quotes="quotes" @deletedQuote="onDeletedQuote"></app-quote-list>
    <app-quote-info></app-quote-info>
  </div>
</template>

<script>
  import Header from '@/components/shared/Header'
  import QuoteProgress from '@/components/Quote/QuoteProgress'
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
        if (this.quotes.length >= this.maxQuotes) {
          return alert('You reached out of limit of quotes please delete one to add another')
        }
        this.quotes.push(newQuote)
      },
      onDeletedQuote(deletedQuote) {
        this.quotes.splice(deletedQuote, 1)
      }
    },
    components: {
      'app-header': Header,
      'app-quote-progress': QuoteProgress,
      'app-quote-form': QuoteForm,
      'app-quote-list': QuoteList,
      'app-quote-info': QuoteInfo
    }
  }
</script>
