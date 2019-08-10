<template>
    <div id="app">
        <Header/>
        <Main/>
        <Footer/>
    </div>
</template>

<script>
    import Header from './views/appLayout/Header'
    import Main from './views/appLayout/Main'
    import Footer from './views/appLayout/Footer'

    export default {
        name: "App",
        components: {
            Header,
            Main,
            Footer
        }
    }
</script>

<style>
    * {
        margin: 0;
        padding: 0;
        border: 0;
    }

    *, *:before, *:after {
        box-sizing: border-box;
    }

    body {
        line-height: 1;
    }

    html, body {
        background: #1B1F23;
        height: 100%;
    }

    body, input, button, select, textarea {
        font-family: "inter", mono, sans-serif;
        font-size: 16px;
        line-height: 1.5;
        font-weight: normal;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        font-smoothing: antialiased;
        color: #fff;
    }

    article, aside, details, figcaption, figure, footer, header, hgroup, menu, nav, section, main, audio, canvas, video, svg {
        display: block;
    }

    img {
        height: auto;
        max-width: 100%;
        display: block;
    }

    a, .a {
        color: inherit;
        text-decoration: none;
        transition: all .4s ease-in-out;
    }

    ol, ul {
        list-style: none;
    }

    #app {
        height: 100%;
    }

    .container {
        width: 980px;
        margin-right: auto;
        margin-left: auto;
    }

    .pt-7 {
        padding-top: 70px !important;
    }

    .pb-3 {
        padding-bottom: 12px !important;
    }
    
    @media (min-width: 800px) {
        .container {
            width: 100%;
            padding-left: 36px;
            padding-right: 36px;
        }
    }

    @media (min-width: 1240px) {
        .container {
            width: 100%;
            padding-left: 48px;
            padding-right: 48px;
            margin-left: 0;
            margin-right: 0;
        }
    }


</style>
