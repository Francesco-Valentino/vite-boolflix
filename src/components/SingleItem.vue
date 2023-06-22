<template>
    <div>
        <h1>
            {{ item.title }}
        </h1>

        <h2>
            {{ item.original_title }}
        </h2>

        <h4>
            {{ item.original_language }}
        </h4>

        <h4>
            {{ item.vote_average }}
        </h4>
    </div>
</template>

<script>
export default {
    name: "SingleItem",

    props: {
        item: Object,
    }
}
</script>

<style lang="scss" scoped>
    
</style>