<template>
  <div class="container">
    <app-header :quoteCount="quotes.length" :maxQuotes="maxQuotes"></app-header>
    <app-new-quote @quoteWasAdded="newquote"></app-new-quote>
    <app-quote-grid :quotes="quotes"></app-quote-grid>
  </div>
</template>

<script>
  import QuoteGrid from './components/QuoteGrid.vue';
  import NewQuote from './components/NewQuote.vue';
  import Header from './components/Header.vue';

  export default {
    data: function() {
      return {
        quotes: [
          'hi there it is a quote'
        ],
        maxQuotes: 10
      }
    },
    methods: {
      newquote(quote) {
        if(this.quotes.length >= 10) {
          return alert('delete some quotes');
        }
        this.quotes.push(quote);
      }
    },
    components: {
      appQuoteGrid: QuoteGrid,
      appNewQuote: NewQuote,
      appHeader: Header
    }
  }
</script>

<style>

</style>
