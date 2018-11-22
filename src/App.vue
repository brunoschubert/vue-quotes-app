<template>
    <div class="container">
        <app-new-quote v-on="quoteAdded($event)"></app-new-quote>
       <app-quote-grid :quotes="quotes"></app-quote-grid> 
    </div>
</template>

<script>
    import QuoteGrid from './components/QuoteGrid.vue';
    import NewQuote from './components/NewQuote.vue';

    export default {
        data: function() {
            return {
                quotes: [
                    'A simple quote'
                ],
                maxQuotes: 10
            }
        },
        methods: {
            newQuote(quote){
                this.quotes.push(quote);
            }
        },
        components: {
            appQuoteGrid: QuoteGrid,
            appNewQuote: NewQuote
        }
    }
</script>

<style>
</style>
