<template>
    <div>
        <h1>
            {{ item.title }}
        </h1>

        <h2>
            {{ item.original_title }}
        </h2>

        <img v-if="item.original_language === 'en'" src='https://upload.wikimedia.org/wikipedia/commons/thumb/a/a4/Flag_of_the_United_States.svg/1200px-Flag_of_the_United_States.svg.png' alt="American Flag">

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
    img{
        width: 50px;
    }
</style>