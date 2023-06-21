<template>
    <div>
        <input type="text" v-model="store.searchText">

        <button>
            Search
        </button>
    </div>
</template>

<script>
import { store } from '../store.js';

export default {
    name: "AppSearchbar",

    data(){
        return{
            store,
        }
    }
}
</script>

<style lang="scss" scoped>
    
</style>