<template>
  <div v-if="quotes.length" class="row mt-5">
    <app-quote-item v-for="(quote, i) in quotes" v-bind:key="i" @click.native="deleteQuote(i)">{{ quote }}</app-quote-item>
  </div>
</template>

<script>
  import QuoteItem from '@/components/Quote/QuoteItem'

  export default {
    props: {
      quotes: Array
    },
    methods: {
      deleteQuote (i) {
        this.$emit('deletedQuote', i)
      }
    },
    components: {
      'app-quote-item': QuoteItem
    }
  }
</script>
