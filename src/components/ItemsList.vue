<template>
    <div>
        <SingleItem v-for="item in items"
        />
    </div>
</template>

<script>
import SingleItem from './SingleItem.vue';
import { store } from '../store.js';


export default {
    name: "ItemsList",

    data(){
        return{
            store
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