<script>
import AppComics from './AppComics.vue'

export default {
    name: 'AppContent',
    components: {
        AppComics
    },
    data() {
        return {

            comics: [

                {
                    "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book",
                },
                {
                    "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book",
                },
                {
                    "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel",
                },
                {
                    "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel",
                },
            ]

        }
    },

}
</script>


<template>
    <main>
        <div id="hero-bg">
        </div>
        <div class="section-container">
            <div id="curr-s">
                <h2>current series</h2>
            </div>
            <AppComics v-for="currentComics in comics " :comicImage='currentComics.thumb'
                :comicTitle="currentComics.series"></AppComics>

            <button>
                <h3>load more</h3>
            </button>
        </div>
    </main>
</template>

<style lang="scss">
@use '../_mixins.scss' as *;
@use '../variables' as *;

#current-s-position {
    @include my-aria-space;
    position: relative;
}


main {
    background-color: rgb(10, 10, 10);
    padding: 0;

    #curr-s {
        width: 200px;
        position: absolute;
        top: -30px;
        left: 0;

        background-color: $universalBlueColor;
        font-size: 1rem;
        text-align: center;
        text-transform: uppercase;
        font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;

        h2 {
            margin: 0;
            padding: 10px 0 10px 0;
        }

    }

    #hero-bg {
        background-image: url('/src/assets/jumbotron.jpg');
        background-size: cover;
        background-position: top;
        height: 400px;
        width: 100%;
    }

    .section-container {
        position: relative;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-around;
        padding: 50px 0 50px 0;

        align-items: flex-start;

        button {
            background-color: $universalBlueColor;

            &:hover {
                background-color: $universalBlueColor;


            }

            h3 {
                @include my-h3-style;
                padding: 0;
                margin: 0;
            }
        }
    }
}

main div h3 {
    @include my-h3-style;
    padding: 50px 0 50px 0;
}
</style>