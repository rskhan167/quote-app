<template>
  <div>
    <app-header :quoteCount="quotes.length" :maxCount="maxQuotes"></app-header>
    <app-new-quote @quoteAdded="newQuote"></app-new-quote>
    <app-quote-grid :quotes="quotes" @quoteDeleted="quoteDelete"></app-quote-grid>
    <div class="info">
      <h3>Info: Click on a quote to delete it</h3>
    </div>
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
        'Just a quote to get started!'
      ],
      maxQuotes: 10
    }
  },
  methods: {
    newQuote(quote){
      if(this.quotes.length >= this.maxQuotes){
        alert('First delete some quotes!');
      }
      else{
        this.quotes.push(quote);
      }
    },
    quoteDelete(index){
      this.quotes.splice(index, 1);
    }
  },
  components:{
    appQuoteGrid: QuoteGrid,
    appNewQuote: NewQuote,
    appHeader: Header
  }
}
</script>

<style scoped>
  .info{
    text-align: center;
    background-color: cadetblue;
    color: white;
  }
</style>
