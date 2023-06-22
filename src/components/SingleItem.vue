<template>
    <div>
        <h1>
            {{ item.title }}
        </h1>

        <h2>
            {{ item.original_title }}
        </h2>

        <img v-if="item.original_language === 'en'" src='https://upload.wikimedia.org/wikipedia/commons/thumb/a/a4/Flag_of_the_United_States.svg/1200px-Flag_of_the_United_States.svg.png' alt="American Flag">

        <img v-else-if="item.original_language === 'it'" src='https://upload.wikimedia.org/wikipedia/commons/thumb/0/03/Flag_of_Italy.svg/1200px-Flag_of_Italy.svg.png' alt="Italian Flag">

        <img v-else-if="item.original_language === 'fr'" src='https://upload.wikimedia.org/wikipedia/commons/thumb/b/bc/Flag_of_France_%281794%E2%80%931815%2C_1830%E2%80%931974%2C_2020%E2%80%93present%29.svg/1280px-Flag_of_France_%281794%E2%80%931815%2C_1830%E2%80%931974%2C_2020%E2%80%93present%29.svg.png' alt="French Flag">

        <img v-else-if="item.original_language === 'es'" src='https://upload.wikimedia.org/wikipedia/commons/thumb/7/7d/Flag_of_Spain_%281785%E2%80%931873%2C_1875%E2%80%931931%29.svg/1200px-Flag_of_Spain_%281785%E2%80%931873%2C_1875%E2%80%931931%29.svg.png' alt="Spanish Flag">

        <img v-else-if="item.original_language === 'de'" src='https://upload.wikimedia.org/wikipedia/commons/thumb/b/ba/Flag_of_Germany.svg/1920px-Flag_of_Germany.svg.png' alt="German Flag">

        <img v-else-if="item.original_language === 'ja'" src='https://upload.wikimedia.org/wikipedia/commons/thumb/9/9e/Flag_of_Japan.svg/1280px-Flag_of_Japan.svg.png' alt="Japanese Flag">

        <p v-else>
            {{ item.original_language }}
        </p>

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