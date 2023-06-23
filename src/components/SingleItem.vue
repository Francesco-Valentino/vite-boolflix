<template>
    <div class="singleCard col-3 m-4 position-relative">
        <img class="itemCover" :src="'https://image.tmdb.org/t/p/w780' + itemImage" :alt="itemName + ' poster'">
        
        <div class="info position-absolute">
            <h1>
                {{ itemName }}
            </h1>

            <h2 v-if="itemName !== itemOriginalName">
                {{ itemOriginalName }}
            </h2>

            <div>
                <img class="flag" v-if="itemLanguage === 'en'" src='https://upload.wikimedia.org/wikipedia/commons/thumb/a/a4/Flag_of_the_United_States.svg/1200px-Flag_of_the_United_States.svg.png' alt="American Flag">

                <img class="flag" v-else-if="itemLanguage === 'it'" src='https://upload.wikimedia.org/wikipedia/commons/thumb/0/03/Flag_of_Italy.svg/1200px-Flag_of_Italy.svg.png' alt="Italian Flag">

                <img class="flag" v-else-if="itemLanguage === 'fr'" src='https://upload.wikimedia.org/wikipedia/commons/thumb/b/bc/Flag_of_France_%281794%E2%80%931815%2C_1830%E2%80%931974%2C_2020%E2%80%93present%29.svg/1280px-Flag_of_France_%281794%E2%80%931815%2C_1830%E2%80%931974%2C_2020%E2%80%93present%29.svg.png' alt="French Flag">

                <img class="flag" v-else-if="itemLanguage === 'es'" src='https://upload.wikimedia.org/wikipedia/commons/thumb/7/7d/Flag_of_Spain_%281785%E2%80%931873%2C_1875%E2%80%931931%29.svg/1200px-Flag_of_Spain_%281785%E2%80%931873%2C_1875%E2%80%931931%29.svg.png' alt="Spanish Flag">

                <img class="flag" v-else-if="itemLanguage === 'de'" src='https://upload.wikimedia.org/wikipedia/commons/thumb/b/ba/Flag_of_Germany.svg/1920px-Flag_of_Germany.svg.png' alt="German Flag">

                <img class="flag" v-else-if="iitemLanguage === 'ja'" src='https://upload.wikimedia.org/wikipedia/commons/thumb/9/9e/Flag_of_Japan.svg/1280px-Flag_of_Japan.svg.png' alt="Japanese Flag">
            
                <p v-else>
                    {{ itemLanguage }}
                </p>
            </div>

            <p class="stars" v-if="Math.round(itemRating / 2) === 0">
                &#9734; &#9734; &#9734; &#9734; &#9734;
            </p>

            <p class="stars" v-if="Math.round(itemRating / 2) === 1">
                &#9733; &#9734; &#9734; &#9734; &#9734;
            </p>

            <p class="stars" v-if="Math.round(itemRating / 2) === 2">
                &#9733; &#9733; &#9734; &#9734; &#9734;
            </p>

            <p class="stars" v-if="Math.round(itemRating / 2) === 3">
                &#9733; &#9733; &#9733; &#9734; &#9734;
            </p>

            <p class="stars" v-if="Math.round(itemRating / 2) === 4">
                &#9733; &#9733; &#9733; &#9733; &#9734;
            </p>

            <p class="stars" v-if="Math.round(itemRating / 2) === 5">
                &#9733; &#9733; &#9733; &#9733; &#9733;
            </p>
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
    img.flag{
        width: 50px;
        height: 25px;
    }

    img.itemCover{
        width: 100%;
        height: 100%;
        object-fit: cover;
        transition: .25s linear;
    }

    p.stars{
        color: yellow;
    }

    div.info{
        color: white;
        top: 8rem;
        left: .5rem;
        display: none;
    }

    div.singleCard:hover img.itemCover{
        filter: brightness(.1);
    }

    div.singleCard:hover div.info{
        display: block;
    }
</style>