<template>
  <div class="container text-center">
    <h1>{{ pageName }}</h1>
    <p>{{ pageDes }}</p>
  </div>
</template>

<script>
export default {
  name: "About",
  data() {
    return {
      pageName: "About Me",
      pageDes: "Welcome In About Me",
    }
  }
};
</script>
