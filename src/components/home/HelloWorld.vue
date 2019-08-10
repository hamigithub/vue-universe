<template>
    <div class="hello">
        <div class="container pt-7 pb-3">
            <h1>Gayhub Universe 2019</h1>
            <p>PHP is the best language in the world!!!</p>
            <ul>
                <li><img src="../../assets/img/szew.jpg" alt=""></li>
            </ul>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'HelloWorld',
        props: {
            msg: String
        }
    }
</script>

<style scoped>
    img {
        width: 200px;
    }

    .container {
        width: 94%;
        margin-left: auto;
        margin-right: auto;
        max-width: 1356px;
        transition: max-width .4s ease-in-out;
    }


</style>
