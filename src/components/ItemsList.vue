<template>
    <div>
        <h2>
            ITEMS LIST
        </h2>

        <SingleItem/>
    </div>
</template>

<script>
import SingleItem from './SingleItem.vue';
import { store } from '../store.js';


export default {
    name: "ItemsList",
    
    components:{
        SingleItem,
    }
}
</script>

<style lang="scss" scoped>
    
</style>