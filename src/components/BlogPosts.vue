<template>
  <div class="post_card">
    <div class="row">
        <div class="col-md-5">
            <img src="../assets/intro.jpg" alt="">
        </div>
        <div class="col-md-6 content-box">
        <h3 class="post_title">{{ title }}</h3>
        <div class="row info">
            <div class="col-sm-4 col-4">
                <div class="post_author">
                    <font-awesome-icon icon="pen"></font-awesome-icon> 
                    {{ author }}
                    </div>
            </div>
            <div class="col-sm-4 col-4">
                <font-awesome-icon icon="calendar"></font-awesome-icon>
                {{ data }}
            </div>
            <div class="col-sm-4 col-4">
                <div class="post_cate">
                    <font-awesome-icon icon="book"></font-awesome-icon> 
                    {{ category }}
                    </div>
            </div>
        </div>
        <p class="post_content">{{ content }}</p>
        <a href="#" class="lnik">Read More <font-awesome-icon icon="angle-double-right"></font-awesome-icon></a>       
        </div>
    </div>  
  </div>
</template>

<script>
export default {
    name: "posts",
    props: ["title", "content", "author", "category", "img", "data"]
}
</script>
<style lang="scss" scoped>
.post_card {
    margin-bottom: 20px;
    background-color: white;
    border-radius: 16px;
    overflow: hidden;
    box-shadow: 0 2px 15px rgb(0, 0, 0, 10%);
    transition: transform var(--main-transition), boxshadow var(--main-transition);

    &:hover {
        transform: translateY(-10px);
        transform: translateX(-10px);
        box-shadow: 0 2px 15px rgb(0, 0, 0, 20%);
    }

        img {
        max-width: 100%;   
    }

    .content-box {
        margin: 15px;
        

        .post_title {
            display: block;
            margin-bottom: 10px;
            color: var(--secondary);
        }

        .post_content {
            width: fit-content;
            margin: 15px 0 10px;
            font-family: sans-serif;
            line-height: 1.5;
            color: var(--grey);
        }

        a {
            text-decoration: none;
            color: var(--secondary)
        }
        .info {
            font-family: Arial;
            font-size: 0.9em;
            line-height: 1.8;
            font-weight: 500;
            color: var(--grey)
        }
    }
}
</style>