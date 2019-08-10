<template>
    <footer class="site-footer">
        <div class="container">
            <a class="site-footer-logo" href="/">
                <img src="../../assets/img/GitHub-Universe-logo-2019.svg" alt="GitHub Universe Logo">
            </a>
            <ul>
                <li>
                    <a href="/code-of-conduct">Code of Conduct</a>
                </li>
                <li>
                    <a href="/terms">Terms</a>
                </li>
                <li>
                    <a href="https://help.github.com/en/articles/github-privacy-statement" target="_blank"
                       rel="noopener noreferrer">Privacy</a>
                </li>
                <li>
                    <a href="https://event-sponsorship.github.com/events/universe/" target="_blank"
                       rel="noopener noreferrer">Event sponsorship</a>
                </li>
                <li>
                    <a href="https://githubuniverse.com/2018/">GitHub Universe 2018</a>
                </li>
            </ul>
        </div>
    </footer>
</template>

<script>
    export default {
        name: "Footer"
    }
</script>

<style scoped>
    .site-footer {
        position: relative;
        width: 100%;
        border-top: 1px solid #2F363D;
        overflow: hidden;
        z-index: 3;
        color: #6A737D;
        font-size: 14px;
        padding-top: 16px;
    }

    .container {
        width: 94%;
        margin-left: auto;
        margin-right: auto;
        max-width: 1356px;
        transition: max-width .4s ease-in-out;
    }

    .container::before {
        display: table;
        content: "";
    }

    .site-footer-logo {
        width: 100px;
        display: block;
    }

    .site-footer ul {
        margin: 16px 0;
    }

    .site-footer ul a {
        display: inline-block;
        color: #6A737D;
        font-family: "fira", mono, sans-serif;
    }

    .site-footer ul a:hover {
        color: #2188FF;
    }

    @media (min-width: 800px) {
        .site-footer {
            padding-left: 256px;
            font-size: 12px;
            padding-top: 0;
        }

        .container {
            width: 100%;
            padding-left: 36px;
            padding-right: 36px;
        }

        .site-footer-logo {
            width: 91px;
            margin-top: 24px;
        }

        .site-footer ul {
            flex-grow: 1;
        }

        .site-footer ul li {
            display: inline-block;
        }

        .site-footer ul li + li:before {
            content: '|';
            margin: 0;
        }

        .site-footer ul li a {
            margin: 0 4px;
        }
    }
</style>
