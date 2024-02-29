<script>
export default {
    name: 'AppLinks',
    data() {
        return {
            links: [
                {
                    title: 'dc comics',
                    list: [
                        {
                            name: 'characters',
                            url: '#'
                        },
                        {
                            name: 'comics',
                            url: '#'
                        },
                        {
                            name: 'movies',
                            url: '#'
                        },
                        {
                            name: 'tv',
                            url: '#'
                        },
                        {
                            name: 'games',
                            url: '#'
                        },
                        {
                            name: 'videos',
                            url: '#'
                        },
                        {
                            name: 'news',
                            url: '#'
                        }
                    ]
                },
                {
                    title: 'shop',
                    list: [
                        {
                            name: 'shop dc',
                            url: '#'
                        },
                        {
                            name: 'shop dc collectibles',
                            url: '#'
                        },

                    ]
                },
                {
                    title: 'dc',
                    list: [
                        {
                            name: 'terms of use',
                            url: '#'
                        },
                        {
                            name: 'privacy policy (new)',
                            url: '#'
                        },
                        {
                            name: 'ad choices',
                            url: '#'
                        },
                        {
                            name: 'advertising',
                            url: '#'
                        },
                        {
                            name: 'jobs',
                            url: '#'
                        },
                        {
                            name: 'subscriptions',
                            url: '#'
                        },
                        {
                            name: 'talent workshops',
                            url: '#'
                        },
                        {
                            name: 'cpsc certificates',
                            url: '#'
                        },
                        {
                            name: 'ratings',
                            url: '#'
                        },
                        {
                            name: 'shop help',
                            url: '#'
                        },
                        {
                            name: 'contact us',
                            url: '#'
                        },
                    ]
                },
                {
                    title: 'sites',
                    list: [
                        {
                            name: 'dc',
                            url: '#'
                        },
                        {
                            name: 'mad magazine',
                            url: '#'
                        },
                        {
                            name: 'dc kids',
                            url: '#'
                        },
                        {
                            name: 'dc universe',
                            url: '#'
                        },
                        {
                            name: 'dc power visa',
                            url: '#'
                        },
                    ]
                },
            ]


        }
    },

}
</script>


<template>
    <section id="link-section">
        <div id="link-container">
            <div id="link-list-container">
                <div v-for="linkitem in links">
                    <h3>{{ linkitem.title }}</h3>
                    <div id="link-list">
                        <li v-for="currentLink in linkitem.list">
                            <a :href=currentLink.url>{{ currentLink.name }}</a>
                        </li>
                    </div>

                </div>
            </div>
            <div id="logo-container">
                <img src="/src/assets/dc-logo-bg.png" alt="">
            </div>
        </div>

    </section>
</template>

<style lang="scss">
@use '../_mixins.scss' as *;
@use '../variables' as *;

#link-section {
    background-image: url('/src/assets/footer-bg.jpg');
}

#link-container {
    @include my-aria-space;
    justify-content: space-between;

}

#link-list-container {
    padding: 20px 10px 20px 10px;
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    max-height: 400px;
}

#link-container h3 {
    color: rgb(255, 255, 255);
    font-size: 1rem;
    margin: 0;
    padding: 0;

    text-transform: uppercase;

    font-family: Impact, Haettenschweiler, 'Arial Narrow', sans-serif;
}

#link-list {
    list-style: none;
    padding: 0 20px 0 0;
    margin: 0;
}



#link-list li a {
    font-size: 0.7rem;
    text-decoration: none;
    text-transform: capitalize;
    color: rgb(109, 109, 109);

    &:hover {
        color: $universalBlueColor;
    }
}

#logo-container img {
    height: 100%;
    max-width: 25rem;
    margin: 0;
    padding: 0;
    border: 0;
    display: block;
    margin-left: auto;
    margin-right: auto;


}
</style>