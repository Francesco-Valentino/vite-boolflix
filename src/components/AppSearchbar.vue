<template>
    <div>
        <input type="text" v-model="txtInput">

        <button @click="sendInput(), $emit('search')">
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
            txtInput: "",
            store,
        }
    },

    methods: {
        sendInput(){
            console.log(this.txtInput);

            store.searchText = this.txtInput;

            console.log(store.searchText);

            /* this.txtInput = ''; */
        }
    }
}
</script>

<style lang="scss" scoped>
    
</style>