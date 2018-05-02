<template>
    <div class="container">
      <appNewQuote></appNewQuote>
      <appQuoteGrid :quotes="quotes"></appQuoteGrid>
    </div>
</template>

<script>
  import QuoteGrid from './components/QuoteGrid.vue'
  import NewQuote from './components/NewQuote.vue'
  
  export default {
    components: {
      appQuoteGrid: QuoteGrid,
      appNewQuote: NewQuote
    },
    data: function() {
      return {
        maxQuotes: 10,
        quotes: [
          'Just to see something'
        ]
      }
    }
  }
</script>

<style>
</style>
