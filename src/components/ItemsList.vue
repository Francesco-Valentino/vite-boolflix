<template>
    <div>
        <SingleItem v-for="item in items"
        :itemName="item.title"
        :itemOriginalName="item.original_title"
        :itemLanguage="item.original_language"
        :itemRating="item.vote_average"/>
    </div>
</template>

<script>
import SingleItem from './SingleItem.vue';
import { store } from '../store.js';


export default {
    name: "ItemsList",

    data(){
        return{
            store,
        }
    },
    
    components:{
        SingleItem,
    },

    props: {
        items: Array,
    },
}
</script>

<style lang="scss" scoped>
    
</style>