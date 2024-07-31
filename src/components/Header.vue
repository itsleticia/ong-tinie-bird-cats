<template>
  <header class="header">
    <div class="container">
      <div class="logo">
        <img src="@/assets/images/logo.png" alt="Logo" />
        <img src="@/assets/images/ong-tinie-bird-cats.png" alt="ong" />
      </div>
      <nav class="menu">
        <ul>
          <li><a href="#">Home</a></li>
          <li><a href="#">Sobre</a></li>
          <li><a href="#">Quero Ajudar</a></li>
          <li><a href="#">Notícias</a></li>
          <li><a href="#">Contato</a></li>
        </ul>
        <Button buttonType="primary" @click="handleButtonClick"
          >Quero adotar</Button
        >
      </nav>
    </div>

    <!-- Carrossel -->
    <div id="carouselExampleIndicators" class="carousel slide">
      <div class="carousel-indicators">
        <button
          type="button"
          data-bs-target="#carouselExampleIndicators"
          data-bs-slide-to="0"
          class="active"
          aria-current="true"
          aria-label="Slide 1"
        ></button>
        <button
          type="button"
          data-bs-target="#carouselExampleIndicators"
          data-bs-slide-to="1"
          aria-label="Slide 2"
        ></button>
        <button
          type="button"
          data-bs-target="#carouselExampleIndicators"
          data-bs-slide-to="2"
          aria-label="Slide 3"
        ></button>
      </div>
      <div class="carousel-inner">
        <div class="carousel-item active">
          <div class="carousel-caption">
            <h5>Doe amor, doe o seu lar!<br />Adote um gatinho</h5>
            <Button buttonType="primary" @click="handleButtonClick"
              >Quero adotar</Button
            >
          </div>
          <img
            src="@/assets/images/banner-gato.png"
            class="d-block w-100"
            alt="Slide 1"
          />
        </div>
        <div class="carousel-item">
          <div class="carousel-caption">
            <h5>Doe amor, doe o seu lar!<br />Adote um gatinho</h5>
            <Button buttonType="primary" @click="handleButtonClick"
              >Quero adotar</Button
            >
          </div>
          <img
            src="@/assets/images/banner-gato.png"
            class="d-block w-100"
            alt="Slide 2"
          />
        </div>
        <div class="carousel-item">
          <div class="carousel-caption">
            <h5>Doe amor, doe o seu lar!<br />Adote um gatinho</h5>
            <Button buttonType="primary" @click="handleButtonClick"
              >Quero adotar</Button
            >
          </div>
          <img
            src="@/assets/images/banner-gato.png"
            class="d-block w-100"
            alt="Slide 3"
          />
        </div>
      </div>
      <button
        class="carousel-control-prev"
        type="button"
        data-bs-target="#carouselExampleIndicators"
        data-bs-slide="prev"
      >
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Previous</span>
      </button>
      <button
        class="carousel-control-next"
        type="button"
        data-bs-target="#carouselExampleIndicators"
        data-bs-slide="next"
      >
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Next</span>
      </button>
    </div>
  </header>
</template>

<script>
import Button from "./Button.vue";

export default {
  components: {
    Button,
  },
  methods: {
    handleButtonClick() {
      console.log("Button clicked");
    },
  },
};
</script>

<style scoped lang="scss">
@import "@/assets/styles/variables.scss";

.header {
  background-color: $color-background;
  padding: 10px 0px; 
  box-sizing: border-box; 
  
}

.container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin: 0.5rem auto;
}

.logo {
  display: flex;
  align-items: center;
}
.logo img {
  margin-right: 1rem;
  height: 2.5rem;
}

.menu {
  flex: 1 1 auto;
  display: flex;
  justify-content: center;
  
  ul {
    display: flex;
    list-style: none;
    margin: 0;
    padding: 0;

    li {
      margin: 0 1rem;

      a {
        text-decoration: none;
        color: $color-text;
        font-size: 1rem;
      }
    }
  }
}
.carousel-item {
  width: 100%; 
}
.carousel-control-prev,
.carousel-control-next {
  display: none;
}
.carousel-inner {
  height: 400px;
  object-fit: cover;
  overflow: hidden;
}

.carousel-inner img {
  width: 100%;
  height: auto;
  max-height: 400px;
  object-fit: contain;
  margin-left: 10rem;
}

#carouselExampleIndicators {
  background-color: $color-soft-pink;
}
.carousel-caption {
  position: absolute;
  top: 50%;
  left: 30%;
  transform: translate(-50%, -30%);
  color: $color-text;
}
</style>
