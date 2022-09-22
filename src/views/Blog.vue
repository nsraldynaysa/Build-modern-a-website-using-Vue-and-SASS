<template>
  <div class="our-blog">
    <div class="blog-intro d-flex justify-content-center align-items-center">
      <div class="container text-center">
        <h1>{{ pageName }}</h1>
        <p class="mt-3">{{ pageDes }}</p>
        <button type="submit" class="btn btn-danger mt-3">Hire me</button>
      </div>
    </div>
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-md-10">
          <div class="posts-area mt-5 mb-5">
            <BlogPosts
              v-for="post in posts"
              :key="post.id"
              :title="post.title"
              :content="post.content"
              :author="post.author"
              :category="post.category"
              :img="post.img"
              :data="post.data"
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import BlogPosts from "../components/BlogPosts.vue";
import JsonPosts from "../json/allposts.json";

export default {
  name: "Blog",
  components: {
    BlogPosts,
  },
  data() {
    return {
      pageName: "Welcome To Architecture Blog",
      pageDes:
        "Lorem ipsum dolor sit amet consectetur adipisicing elit. Saepe, iusto amet consectetur.",
      posts: JsonPosts,
    };
  },
};
</script>
<style lang="scss" scoped>
.our-blog {
  margin: 0;

  .blog-intro {
    position: relative;
    background-color: var(--tertiary);
    height: 60vh;
    margin: 0;

    p {
      font-family: Arial;
      margin-top: 2em;
      font-size: 1.2em;
      line-height: 1.8;
      font-weight: 500;
      color: var(--grey);
    }
  }
}
</style>
