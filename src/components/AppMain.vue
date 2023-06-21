<template>
    <main>
        <h1>
            APP MAIN
        </h1>

        <ItemsList/>
    </main>
</template>

<script>
import ItemsList from './ItemsList.vue';
import axios from 'axios';
import { store } from '../store.js';

export default {
    name: "AppMain",

    data(){
        return{
            store,
        }
    },
    
    components:{
        ItemsList,
    },

    created() {
        axios.get('https://api.themoviedb.org/3/search/movie?api_key=388bc42a36d295b0d1d3ccd86ca4779e&query=drive')
            .then(function (response) {
            console.log(response);
            })
        .catch(function (error) {
            console.log(error);
        })
    },
}
</script>

<style lang="scss" scoped>
    
</style>