<template>
    <main id="content" class="main page-content">
        <router-view></router-view>
    </main>
</template>

<script>
    export default {
        name: "Main",
        data() {
            return {
                imgItem: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
            }
        }
    }
</script>

<style scoped>
    main#content {
        opacity: 0;
        transition: opacity 0.3s ease;
    }

    body.page-ready main#content {
        opacity: 1;
    }

    main#content {
        opacity: 1;
    }

    @media (min-width: 800px) {
        main#content {
            padding-left: 256px;
        }
    }

</style>
