<template>
  <header class="header">
      <div class="container">
          <div class="logo">Towner</div>
        <ul class="nav">
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
        <div class="socail-header d-flex justify-content-center align-items-center">
            <font-awesome-icon :icon="['fab', 'instagram']" size="2x" />
            <button type="submit" class="btn btn-danger" id="colFormLabelSm">
            Subscribe
        </button>
        </div>
      </div> 
  </header>
</template>

<script>
export default {
    name: 'AppHeader',
}
</script>

<style lang="scss" scoped>
  .header {
        background-color: var(--dark);

        .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 72px;

            .logo {
                font-size: 22px;
                color: var(--light);
                font-weight: 100;
                text-align: center;
                text-transform: uppercase;
            }

            .nav {
                display: flex;
                justify-content: flex-start;
                align-items: center;

                
                a {
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    position: relative;
                    height: 72px;
                    margin: 15px;
                    text-decoration: none;
                    color: var(--light);
                    overflow: hidden;
                    transition: var(--main-transition);

                    &:before {
                        content: "";
                        position: absolute;
                        width: 100%;
                        height: 4px;
                        background-color: var(--primary);
                        top: 0;
                        left: -100%;
                    }

                    &:hover {
                        color: var(--primary);
                        background-color: var(--light);

                        &:before {
                            left: 0;
                        }
                    }
                }
            }

            .socail-header {
                display: block;
                color: var(--light);

                svg {
                    margin-right: 30px;

                    &:hover {
                        transform: translate(-3px);
                        color: var(--primary)
                    }
                }
            }
        }
    }
</style>