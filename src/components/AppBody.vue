<template>
    <header class="bgBlack">
        <AppSearchbar @search="getMovie(), getTvSeries()"/>        
    </header>

    <main class="bgBlack">
        <ItemsList 
        :items="items"/>

        <SeriesList 
        :series="series"/>
    </main>
</template>

<script>
import AppSearchbar from './AppSearchbar.vue';
import ItemsList from './ItemsList.vue';
import SeriesList from './SeriesList.vue';
import axios from 'axios';
import { store } from '../store.js';

export default {
    name: "AppBody",

    data(){
        return{
            store,
            items: [],
            series: [],
        }
    },

    components: {
        AppSearchbar,
        ItemsList,
        SeriesList,
    },

    methods: {
        getMovie(){
            axios.get('https://api.themoviedb.org/3/search/movie?api_key=388bc42a36d295b0d1d3ccd86ca4779e&query=' + store.searchText)
            .then((response) => {
            console.log(response.data.results);
            this.items = response.data.results;
            console.log(this.items);
            })
            .catch(function (error) {
            console.log(error);
             })
        },

        getTvSeries(){
            axios.get('https://api.themoviedb.org/3/search/tv?api_key=388bc42a36d295b0d1d3ccd86ca4779e&query=' + store.searchText)
            .then((response) => {
            console.log(response.data.results);
            this.series = response.data.results;
            console.log(this.series);
            })
            .catch(function (error) {
            console.log(error);
             })
        }
    }
}
</script>

<style lang="scss" scoped>

</style>