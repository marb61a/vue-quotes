<template>
  <div class="container">
    <div class="row">
      <div class="alert alert-info">
        Info: Click on a Quote to delete it!
      </div>
    </div>
  </div>
</template>

<script>
import Header from './components/Header.vue';

export default {
  name: 'app',
  data: function(){
    return {
      quotes: [
        'An example quote to display'
      ],
      maxQuotes: 10
    }
  },
  methods: {
    newQuote(quote){
      if(this.quotes.length >= this.maxQuotes){
        return alert('Please delete Quotes first!');
      }
      this.quotes.push(quote);
    }
  },
  components: {
    appHeader: Header
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
