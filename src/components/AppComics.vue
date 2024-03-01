<script>
export default {
    name: 'AppComics',
    props: {
        comicImage: String,
        comicTitle: String
    }
}
</script>

<template>
    <div class="comic">
        <img :src="comicImage" alt="comic book cover">
        <p>{{ comicTitle }}</p>
    </div>
</template>

<style lang="scss">
@use '../_mixins.scss' as *;
@use '../variables' as *;


.comic {
    width: calc(100% / 6);
    display: flex;
    flex-direction: column;
    padding: 0 15px 20px 15px;
    overflow: hidden;




    img {
        height: 200px;
        object-fit: cover;
        object-position: top;
    }

    p {
        font-size: 0.8rem;
        text-transform: uppercase;

        font-family: Verdana, Geneva, Tahoma, sans-serif
    }
}
</style>