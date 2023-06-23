<template>
    <div>
        <SingleItem v-for="item in series"
        :itemName="item.name"
        :itemOriginalName="item.original_name"
        :itemLanguage="item.original_language"
        :itemRating="item.vote_average"
        :itemImage="item.poster_path"/>
    </div>
</template>

<script>
import SingleItem from './SingleItem.vue';
import { store } from '../store.js';


export default {
    name: "SeriesList",

    data(){
        return{
            store,
        }
    },
    
    components:{
        SingleItem,
    },

    props: {
        series: Array,
    },
}
</script>

<style lang="scss" scoped>
    
</style>