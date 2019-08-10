<template>
    <header class="site-header">
        <div class="site-header__inner">
            <div class="site-branding">
                <a href="/">
                    <img src="../../assets/img/GitHub-Universe-logo-2019.svg" alt="emm...">
                </a>
            </div>
            <nav class="navigation-drawer">
                <div class="navigation-drawer__inner">
                    <ul class="main-nav">
                        <li :class="isActive===index?'is-active':''" v-for="(item,index) in itemList" :key="index"
                            @click.prevent="getItem(index,item)">
                            <span>{{item.id}}</span>
                            <span>{{item.cn}}</span>
                        </li>
                    </ul>
                </div>
            </nav>
            <div class="site-header__ft">
                <div class="social-title">
                    Subscribe for updates
                </div>
                <div class="social-links">
                    <a href="https://www.baidu.com" target="_blank">
                        <img src="../../assets/img/twitter.svg" alt="twitter">
                    </a>
                    <a href="https://www.baidu.com" target="_blank">
                        <img src="../../assets/img/instagram.svg" alt="instagram">
                    </a>
                    <a href="https://www.baidu.com" target="_blank">
                        <img src="../../assets/img/youtube.svg" alt="youtube">
                    </a>
                </div>
            </div>
        </div>
    </header>
</template>

<script>
    export default {
        name: "Header",
        data() {
            return {
                itemList: [
                    {
                        id: 1,
                        name: "/",
                        cn: "相册"
                    },
                    {
                        id: 2,
                        name: "video",
                        cn: "小电影"
                    }
                ],
                isActive: 0//0为默认选择第一个，-1为不选择
            }
        },
        methods: {
            getItem(index, item) {
                this.isActive = index;
                this.$router.push({path: item.name})
            }
        }
    }
</script>

<style scoped>
    .site-header {
        position: fixed;
        z-index: 10;
        width: 100%;
        left: 0;
        top: 0;
        background: #1B1F23;
        border-bottom: 1px solid #2F363D;
        transition: background .4s ease-in-out, opacity .4s ease-in-out, width 0.2s ease;
    }

    .site-header__inner {
        display: flex;
    }

    .site-branding {
        padding: 0 24px;
    }

    .site-branding a {
        display: block;
        width: 128px;
        transition: width .4s ease-in-out;
        position: relative;
    }

    .site-branding a img {
        width: 100%;
        opacity: 1;
        transition: opacity 1s ease;
    }

    ul.main-nav > li {
        display: block;
        padding: 6px 24px;
        font-size: 14px;
        letter-spacing: 0;
        font-weight: 400;
        color: #fff;
        position: relative;
        cursor: pointer;
        transition: color .4s ease-in-out, height .4s ease-in-out;
    }

    ul.main-nav li.is-active, ul.main-nav li:hover {
        color: #34D058;
    }

    ul.main-nav li.is-active span:last-child:before {
        content: '>';
    }

    ul.main-nav li span:first-child {
        color: #6A737D !important;
        padding-right: 12px;
    }

    .social-title {
        text-align: center;
        padding: 12px;
        border-bottom: 1px solid #2F363D;
    }

    .site-header__ft {
        display: none;
    }

    .social-links {
        display: flex;
        align-items: stretch;
    }

    .social-links a {
        display: flex;
        height: 46px;
        align-items: center;
        justify-content: center;
        width: 33.333%;
        transition: background .4s ease-in-out;
    }

    .social-links a img {
        display: block;
        margin: 0;
    }

    .social-links a + a {
        border-left: 1px solid #2F363D;
    }

    .social-links a:hover {
        background: rgba(0, 0, 0, 0.8);
    }

    @media (min-width: 800px) {
        .site-header {
            border-bottom: none;
            border-right: 1px solid #2F363D;
            width: 256px;
            height: 100%;
        }

        .site-header__inner {
            flex-direction: column;
            height: 100%;
        }

        .site-branding {
            height: 96px;
            display: flex;
            align-items: center;
            border-bottom: 1px solid #2F363D;
        }

        .site-branding a {
            width: 164px;
        }

        .navigation-drawer {
            flex-grow: 1;
        }

        ul.main-nav {
            padding: 24px 0;
        }

        ul.main-nav li {
            margin-bottom: 10px;
        }

        ul.main-nav li.is-active {
            background: #2F363D;
        }

        .site-header__ft {
            display: block;
            border-top: 1px solid #2F363D;
        }
    }
</style>
