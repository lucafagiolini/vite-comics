<script>
export default {
    name: 'AppContent',
    data() {
        return {

        }
    },

}
</script>


<template>
    <main>
        <div class="section-container">
            <h3> -> Content goes here <- </h3>
        </div>
    </main>
</template>

<style lang="scss">
@use '../_mixins.scss' as *;
@use '../variables' as *;

main {
    background-color: rgb(10, 10, 10);
    padding: 0;
}

h3 {
    @include my-h3-style;
    padding: 50px 0 50px 0;
}
</style>