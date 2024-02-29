<script>
export default {
    name: 'AppHeader',
    data() {
        return {
            navLinks: [
                { name: 'characters', path: '#' },
                { name: 'comics', path: '#' },
                { name: 'movies', path: '#' },
                { name: 'tv', path: '#' },
                { name: 'games', path: '#' },
                { name: 'collectibles', path: '#' },
                { name: 'videos', path: '#' },
                { name: 'news', path: '#' },
                { name: 'shop', path: '#' }
            ]
        }
    },

}
</script>


<template>
    <header>
        <div class="white-air">

        </div>
        <div class="section-container">
            <img src="../assets/dc-logo.png" alt="">
            <div id="links-header-nav">
                <ul>
                    <li v-for="link in navLinks" :key="link.name">
                        <a :href="link.path">{{ link.name }}</a>
                    </li>
                </ul>

            </div>
        </div>
        <div class="white-air">
        </div>

    </header>
</template>

<style lang="scss">
@use '../_mixins.scss' as *;
@use '../variables' as *;

.white-air {
    background-color: white;
    height: 3px;
    width: 100%;
}

header {
    background-color: white;
    padding: 0;
}

img {
    height: 70px;

}

links-header-nav {
    height: 100%;
}

#links-header-nav ul {
    display: flex;
    padding: 0 2rem 0 2rem;
    margin: 0;
    height: 100px;
}

#links-header-nav ul li {
    display: flex;
    height: 100%;
    padding: 0 0.7rem 0 0.7rem;
    align-items: center;

    &:hover {
        border-bottom: 3px solid $universalBlueColor;
    }

}



.section-container {
    @include my-aria-space;
    justify-content: space-between // temporary fixfor the mix-in
}

a {
    @include my-anchor;
    color: rgb(20, 20, 20);
    text-transform: uppercase;

    &:hover {
        color: $universalBlueColor;
    }
}
</style>