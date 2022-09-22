<template>
  <main class="home-page">
    <div class="landing">
      <div class="container text-left">
        <div class="hiro">
          <h1>{{ pageName }}</h1>
          <p>{{ pageDes }}</p>
        </div>
      </div>
    </div>
    <div class="about pt-5 pb-5">
      <div class="container d-flex justify-content-center">
        <div class="box-content text-center">
          <h3 class="main-title">About me</h3>
          <span>Architecture blog</span>
          <p>
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Nisi
            corporis ab unde ullam, assumenda delectus, cum amet quasi dolores
            ipsum at id. Inventore illum magnam aliquam dignissimos eligendi
            aspernatur ipsa.
          </p>
        </div>
      </div>
    </div>

    <div class="gallery pt-5 pb-5">
      <div class="container text-center">
        <h3 class="main-title">Latest articles</h3>
        <span>Most recent posts</span>
        <div class="row pt-5 mt-5">
          <div class="col-md-3 col-sm-6">
            <div class="card text-white">
              <img
                src="../assets/artic-01.jpg"
                alt="Image"
                class="img_gallery"
              />
              <div
                class="card-img-overlay d-flex justify-content-center align-items-end"
              >
                <h5 class="card-title">Flatiron Bulding</h5>
              </div>
            </div>
          </div>
          <div class="col-md-3 col-sm-6">
            <div class="card text-white">
              <img
                src="../assets/artic-02.jpg"
                alt="Image"
                class="img_gallery"
              />
              <div
                class="card-img-overlay d-flex justify-content-center align-items-end"
              >
                <h5 class="card-title">Empire State</h5>
              </div>
            </div>
          </div>
          <div class="col-md-3 col-sm-6">
            <div class="card text-white">
              <img
                src="../assets/artic-03.jpg"
                alt="Image"
                class="img_gallery"
              />
              <div
                class="card-img-overlay d-flex justify-content-center align-items-end"
              >
                <h5 class="card-title">Rockefeller</h5>
              </div>
            </div>
          </div>
          <div class="col-md-3 col-sm-6">
            <div class="card text-white">
              <img
                src="../assets/artic-04.jpg"
                alt="Image"
                class="img_gallery"
              />
              <div
                class="card-img-overlay d-flex justify-content-center align-items-end"
              >
                <h5 class="card-title">Towers laz</h5>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="news-letters pt-5 pb-5">
      <div class="container text-center">
        <h3 class="main-title">News letters</h3>
        <span>Sing up to News letters</span>
        <form class="form-inline d-flex justify-content-center mt-5 mb-5">
          <div class="form-group d-flex justify-content">
            <input
              v-model="inputEmail"
              type="email"
              class="form-control"
              id="colFormLabelSm"
              placeholder="Enter your email address"
            />
            <button
              type="submit"
              class="btn btn-danger d-flex align-items-center"
            >
              Subscribe
              <font-awesome-icon icon="paper-plane"></font-awesome-icon>
            </button>
          </div>
        </form>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      pageName: "Towner",
      pageDes:
        "Our works of therapists is hero to help you with anxiety, stats depreision or loss",
      imageSrc: "../assets/artic-01.jpg",
      inputEmail: null,
    };
  },
};
</script>

<style lang="scss" scoped>
.landing {
  position: relative;
  background-image: url(../assets/intro.jpg);
  background-size: cover;
  height: calc(100vh - 72px);
  display: flex;
  justify-content: start;
  align-items: center;

  .hiro {
    position: absolute;
    width: 400px;

    h1 {
      font-family: sans;
      font-size: 45pt;
      font-weight: bold;
      color: var(--dark);
      margin: 0;
    }

    p {
      font-family: Arial;
      margin-top: 2em;
      font-size: 1.2em;
      line-height: 1.8;
      font-weight: 500;
      color: var(--drak);
    }
  }
}
.about {
  background-color: white;

  .box-content {
    width: 520px;
  }

  p {
    font-family: Arial;
    margin-top: 2em;
    font-size: 1.2em;
    line-height: 1.8;
    font-weight: 500;
    color: var(--drak);
  }
}
.gallery {
  .card {
    margin-bottom: 20px;
    padding: none;
    border: none;
    border-radius: none;
    transition: transform var(--main-transition),
      boxshadow var(--main-transition);

    img {
      widows: 100%;
      border-radius: 20px;
      box-shadow: 0 2px 15px rgb(0, 0, 0, 10%);
    }
    &:hover {
      transform: translateY(-10px);
    }

    .card-title {
      font-family: Arial;
      font-size: 1.4em;
      line-height: 1.8;
      font-weight: 500;
    }
  }
}
.news-letters {
  background-color: var(--secondary);

  h3 {
    color: var(--light);
  }

  .form-inline {
    display: block;
    width: 100%;
    font-size: 1rem;
    line-height: 1.5;
    background-clip: padding-box;
    padding-top: 2.1rem;

    .form-group {
      background-color: var(--light);
      width: max-content;
      border-radius: 50px;
      border: 1px solid var(--secondary);
      display: inline-block;
      box-shadow: 0 2px 15px var(--drak);

      input[type="email"] {
        background-image: none;
        background-color: transparent;
        border: none;
        padding: 0.375rem 0.75rem;
        outline: none;
      }

      svg {
        margin-left: 5px;
      }
    }
  }
}
</style>
