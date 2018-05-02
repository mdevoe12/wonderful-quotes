<template>
    <div class="container">
      <appNewQuote @quoteAdded="newQuote"></appNewQuote>
      <appQuoteGrid :quotes="quotes" @quoteDeleted="deleteQuote"></appQuoteGrid>
      <div class="row">
        <div class="col-sm-12 text-center">
          <div class="alert alert-info">
            Info: Click on a Quote to delete it.
          </div>
        </div>
      </div>
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
    },
    methods: {
      newQuote(quote) {
        this.quotes.push(quote)
      },
      deleteQuote(index) {
        this.quotes.splice(index, 1)
      }
    }
  }
</script>

<style>
</style>
