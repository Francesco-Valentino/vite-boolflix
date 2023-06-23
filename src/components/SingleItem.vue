<template>
    <div>
        <h1>
            {{ itemName }}
        </h1>

        <h2>
            {{ itemOriginalName }}
        </h2>

        <img :src="'https://image.tmdb.org/t/p/w780' + itemImage" :alt="itemName + ' poster'">

        <img v-if="itemLanguage === 'en'" src='https://upload.wikimedia.org/wikipedia/commons/thumb/a/a4/Flag_of_the_United_States.svg/1200px-Flag_of_the_United_States.svg.png' alt="American Flag">

        <img v-else-if="itemLanguage === 'it'" src='https://upload.wikimedia.org/wikipedia/commons/thumb/0/03/Flag_of_Italy.svg/1200px-Flag_of_Italy.svg.png' alt="Italian Flag">

        <img v-else-if="itemLanguage === 'fr'" src='https://upload.wikimedia.org/wikipedia/commons/thumb/b/bc/Flag_of_France_%281794%E2%80%931815%2C_1830%E2%80%931974%2C_2020%E2%80%93present%29.svg/1280px-Flag_of_France_%281794%E2%80%931815%2C_1830%E2%80%931974%2C_2020%E2%80%93present%29.svg.png' alt="French Flag">

        <img v-else-if="itemLanguage === 'es'" src='https://upload.wikimedia.org/wikipedia/commons/thumb/7/7d/Flag_of_Spain_%281785%E2%80%931873%2C_1875%E2%80%931931%29.svg/1200px-Flag_of_Spain_%281785%E2%80%931873%2C_1875%E2%80%931931%29.svg.png' alt="Spanish Flag">

        <img v-else-if="itemLanguage === 'de'" src='https://upload.wikimedia.org/wikipedia/commons/thumb/b/ba/Flag_of_Germany.svg/1920px-Flag_of_Germany.svg.png' alt="German Flag">

        <img v-else-if="iitemLanguage === 'ja'" src='https://upload.wikimedia.org/wikipedia/commons/thumb/9/9e/Flag_of_Japan.svg/1280px-Flag_of_Japan.svg.png' alt="Japanese Flag">

        <p v-else>
            {{ itemLanguage }}
        </p>

        <div>
            <h4 v-if="Math.round(itemRating / 2) === 0">
                &#9734; &#9734; &#9734; &#9734; &#9734;
            </h4>

            <h4 v-if="Math.round(itemRating / 2) === 1">
                &#9733; &#9734; &#9734; &#9734; &#9734;
            </h4>

            <h4 v-if="Math.round(itemRating / 2) === 2">
                &#9733; &#9733; &#9734; &#9734; &#9734;
            </h4>

            <h4 v-if="Math.round(itemRating / 2) === 3">
                &#9733; &#9733; &#9733; &#9734; &#9734;
            </h4>

            <h4 v-if="Math.round(itemRating / 2) === 4">
                &#9733; &#9733; &#9733; &#9733; &#9734;
            </h4>

            <h4 v-if="Math.round(itemRating / 2) === 5">
                &#9733; &#9733; &#9733; &#9733; &#9733;
            </h4>
        </div>
    </div>
</template>

<script>
export default {
    name: "SingleItem",

    props: {
        itemName: String,
        itemOriginalName: String,
        itemLanguage: String,
        itemRating: Number,
        itemImage: String,
    },
}
</script>

<style lang="scss" scoped>
    img{
        width: 50px;
    }
</style>