<template>
    <div class="footer">
        <div class="container">
            <div class="row">
                <div class="col-md-4">
                    <div class="logo text-center">
                        <a>Towner</a>
                    </div>
                </div>
                <div class="col-md-4">
                    <ul class="menu-nav text-center">
                        <router-link to="/" tag="li" exact>
                        <a>Home</a>
                        </router-link>
                        <router-link to="/about" tag="li">
                        <a>About</a>
                        </router-link>
                        <router-link to="/blog" tag="li">
                        <a>Articles</a>
                        </router-link>
                    </ul>
                </div>
                <div class="col-md-4">
                    <div class="socail d-flex justify-content-center align-items-center">
                        <font-awesome-icon :icon="['fab','twitter']" size="lg" />
                        <font-awesome-icon :icon="['fab','facebook-f']" size="lg" />
                        <font-awesome-icon :icon="['fab','instagram']" size="lg" />
                        <font-awesome-icon :icon="['fab','snapchat-ghost']" size="lg" />
                    </div>
                </div>
            </div>
            <div class="copy-right text-center mt-3">
                <p>Designed with <i class="ml-2 mr-2"><font-awesome-icon icon="heart"></font-awesome-icon></i> Love by NEGM Lab </p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "AppFooter",
    data() {
        return {
            Wideget: 'Title widget',
        }
    },
}
</script>

<style lang="scss" scoped>
.footer {
    background-color: var(--dark);
    margin: 0 auto;

    .logo {
        display: flex;
        justify-content: start;
        align-items: center;
        height: 72px;
        font-size: 22px;
        color: var(--light);
        font-weight: 100;
        text-transform: uppercase;
    }

    .menu-nav {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 72px;
        padding: 0;
        
        a {
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
            height: 72px;
            margin: 15px;
            font-family: Arial;
            font-size: 15px;
            line-height: 1.8;
            text-decoration: none;
            color: var(--light);
            overflow: hidden;
            transition: var(--main-transition);

            &:hover {
                color: var(--primary);

            }
        }
    }
    .socail {
        height: 72px;
        
        svg {
        margin: 20px;
        color: var(--light);

            &:hover {
                color: var(--primary)
            }
        }
    }
    

    .copy-right {
        padding: 20px;

        p {
            font-family: Arial;
            font-size: 15px;
            line-height: 1.8;
            color: var(--light);

            i {
                color: var(--primary)
            }
        }
    }
}
</style>