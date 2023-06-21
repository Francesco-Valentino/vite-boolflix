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

export default {
    name: "AppMain",
    
    components:{
        ItemsList,
    }
}
</script>

<style lang="scss" scoped>
    
</style>