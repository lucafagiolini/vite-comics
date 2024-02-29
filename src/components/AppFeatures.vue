<script>
export default {
    name: 'AppFeatures',
    data() {
        return {
            features: [
                {
                    titile: 'digital comics',
                    img: '/src/assets/buy-comics-digital-comics.png',
                },
                {
                    titile: 'dc mercandise',
                    img: '/src/assets/buy-comics-merchandise.png',
                },
                {
                    titile: 'subscriptions',
                    img: '/src/assets/buy-comics-subscriptions.png',
                },
                {
                    titile: 'comic shop locator',
                    img: '/src/assets/buy-comics-shop-locator.png',
                },
                {
                    titile: 'dc power visa',
                    img: '/src/assets/buy-dc-power-visa.svg',
                }
            ]
        }
    },

}
</script>


<template>
    <section class="bg-color-features">
        <ul>
            <li v-for="feature in features">
                <img :src="feature.img" alt="feature.titile">
                <h3>{{ feature.titile }}</h3>
            </li>
        </ul>
    </section>
</template>

<style lang="scss">
@use '../_mixins.scss' as *;
@use '../variables' as *;

.bg-color-features {
    background-color: $universalBlueColor;
}

section ul {
    @include my-aria-space;
    justify-content: space-evenly;
}

section ul li {
    display: flex;
    flex-wrap: nowrap;
    align-items: center;
    justify-content: center;
    padding: 50px 20px 50px 20px;

    cursor: pointer;

    &:hover {
        transform: scale(1.1);
        transition: transform 0.3s;
    }
}

li img {
    max-height: 50px;
    max-width: 50px;

}

li h3 {
    font-size: 0.9rem;
    padding: 0 1rem 0 1rem;
    text-transform: uppercase;
    font-family: Impact, Haettenschweiler, 'Arial Narrow', sans-serif;
    font-weight: 100;
}
</style>