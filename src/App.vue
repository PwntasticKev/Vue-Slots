<template>
    <div class="container">
        <br>
        <header-bar :quoteCount="quotes.length" :maxquotes="maxQuotes"></header-bar>
        <app-new-quote @quoteAdded="newQuote"></app-new-quote>
        <app-quote-grid :quotes="quotes" @quoteDeleted="quoteDeleted(i)"></app-quote-grid>
        
    </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue'
import NewQuote from './components/NewQuote.vue'
import Header from './components/Header.vue'
    export default {
        data: function() {
            return {
                quotes: ["Just a Quote to see something"],
                maxQuotes: 10
            }
        },
        components: {
            "appQuoteGrid": QuoteGrid,
            "appNewQuote": NewQuote,
            "headerBar": Header
        },
        methods: {
            newQuote(newQuote) {
                if(this.quotes.length >= maxQuotes) {
return alert("please remove some quotes before adding more.")
                }
                this.quotes.push(newQuote)
            },
            quoteDeleted(i) {
                this.quotes.splice(i, 1)
            }
        }
    }
</script>

<style>

</style>
