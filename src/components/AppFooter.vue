<script>
export default {
    name: 'AppLinks',
    data() {

        return {

            socialLinks: [
                {
                    img: '/src/assets/footer-facebook.png',
                },

                {
                    img: '/src/assets/footer-twitter.png',
                },

                {
                    img: '/src/assets/footer-youtube.png',
                },

                {
                    img: '/src/assets/footer-pinterest.png',
                },

                {
                    img: '/src/assets/footer-periscope.png',
                }
            ]
        }
    },
}

</script>


<template>
    <div id="bg-footer">
        <div class="footer-section-container">

            <button class="sign-in-btn">
                <a href="#">sign-up now!</a>
            </button>

            <div id="social-link-container">
                <span>follow us</span>

                <ul>
                    <li v-for="socialItem,  in socialLinks">
                        <a href="#">
                            <img :src=socialItem.img alt="">
                        </a>
                    </li>
                </ul>

            </div>



        </div>
    </div>
</template>

<style lang="scss">
@use '../_mixins.scss' as *;
@use '../variables' as *;

#bg-footer {
    background-color: #303030;
}

.footer-section-container {
    @include my-aria-space;

    justify-content: space-between;
}

.sign-in-btn {
    background-color: transparent;
    color: white;
    padding: 10px 12px;
    border: solid 1px $universalBlueColor;

    &:hover {
        transform: scale(1.1);
        transition: transform 0.3s;
    }

    a {
        text-decoration: none;
        color: white;

        &:hover {
            color: $universalBlueColor;
        }
    }
}

#social-link-container {
    display: flex;
    align-items: center;

    span {
        color: $universalBlueColor;
        text-transform: uppercase;
        font-weight: 500;
        font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
        padding: 0 10px 0 10px;
    }


    ul {

        padding: 0;
        display: flex;
        align-items: center;
        justify-content: space-between;
        list-style-type: none;
    }

    li {
        margin: 0 10px;
        text-decoration: none;



        &:hover {


            transform: scale(1.1);
            transition: transform 0.3s;
        }
    }

    img {

        height: 40px;

        padding: 5px;
        border-radius: 50%;

        &:hover {
            background-color: rgb(40, 40, 40);

            transform: scale(1.1);
            transition: transform 0.3s;
        }
    }
}
</style>