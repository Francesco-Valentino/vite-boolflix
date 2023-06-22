<template>
    
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
            items: [],
        }
    },
    
    components:{
        ItemsList,
    },
}
</script>

<style lang="scss" scoped>
    
</style>