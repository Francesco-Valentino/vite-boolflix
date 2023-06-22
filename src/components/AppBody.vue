<template>
    <header>
        <AppSearchbar/>        
    </header>

    <main>
        <AppMain/>
    </main>
</template>

<script>
import AppSearchbar from './AppSearchbar.vue';
import AppMain from './AppMain.vue';

export default {
    name: "AppBody",

    components: {
        AppSearchbar,
        AppMain
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
        }
    }
}
</script>

<style lang="scss" scoped>
    
</style>