<template>
  <div class="container mt-5">
    <div class="row align-items-center">
      <!-- Formulário -->
      <div class="col-md-6">
        <form @submit.prevent="handleSubmit" class="form-adjusted">
          <h2 class="mb-4">Fale Conosco<br />agora mesmo</h2>
          <div class="mb-3">
            <label for="name" class="form-label"></label>
            <input
              type="text"
              class="form-control"
              id="name"
              name="name"
              placeholder="Nome"
              required
            />
          </div>
          <div class="mb-3">
            <label for="email" class="form-label"></label>
            <input
              type="email"
              class="form-control"
              id="email"
              name="email"
              placeholder="Email"
              required
            />
          </div>
          <div class="mb-3">
            <label for="phone" class="form-label"></label>
            <input
              type="tel"
              class="form-control"
              id="phone"
              name="phone"
              placeholder="Celular"
              required
            />
          </div>
          <div class="mb-3">
            <label for="message" class="form-label"></label>
            <textarea
              class="form-control"
              id="message"
              name="message"
              rows="4"
              placeholder="Mensagem"
              required
            ></textarea>
          </div>
          <Button variant="primary">Enviar Mensagem</Button>
        </form>
      </div>

      <!-- Imagem -->
      <div class="col-md-6 position-relative">
        <img
          src="@/assets/images/gato-form.png"
          alt="Form Image"
          class="img-fluid rounded img-adjusted"
        />
      </div>
    </div>
  </div>

  <!-- Seção de dúvidas -->
  <div class="duvidas">
    <div class="mt-5 text-center">
      <h3>Ainda tem dúvidas?</h3>
      <div class="row mt-4">
        <div class="col-md-4">
          <div class="card">
            <div class="card-body">
              <img src="@/assets/images/email.png" />
              <h5 class="card-title">Por email</h5>
              <p class="card-text">
                Envie a sua mensagem e responderemos em ate 2 dias úteis <br />
                <a href="#">contato@obgtiniebirdcats.com.br</a>
              </p>
            </div>
          </div>
        </div>
        <div class="col-md-4">
          <div class="card whatsapp">
            <div class="card-body">
              <img src="@/assets/images/whatsapp.png" />
              <h5 class="card-title">Por WhatsApp</h5>
              <p class="card-text">Chame no <a href="">(13) 91234-5678</a></p>
            </div>
          </div>
        </div>
        <div class="col-md-4">
          <div class="card">
            <div class="card-body">
              <img src="@/assets/images/coracao.png" />
              <h5 class="card-title">Redes sociais</h5>
              <p class="card-text">
                Utilize nsosas redes sociais para entrar em contaot conosco!
              </p>
              <div class="redes-sociais">
                <a href="#"><img src="@/assets/images/instagram.png" /></a>
                <a href="#"><img src="@/assets/images/facebook.png" /></a>
                <a href="#"><img src="@/assets/images/youtube.png" /></a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Button from "@/components/Button.vue";

export default {
  components: {
    Button,
  },
  methods: {
    handleSubmit() {
      alert("Formulário enviado!");
    },
  },
};
</script>

<style scoped lang="scss">
@import "@/assets/styles/variables.scss";

.container {
  background-color: $color-secondary;
  padding: 0;
  margin: 0;
}

.form-adjusted {
  padding: 30px 50px;
  border-radius: 8px;
  color: $color-background;
  height: auto;
  margin: 0;

  .mb-3,
  .mb-4 {
    margin-bottom: 0 !important;
  }
  h2 {
    font-size: 1.5rem;
  }
}

.img-fluid {
  max-width: 100%;
  height: auto;
}

.img-adjusted {
  position: relative;
}

.form-control {
  border-radius: 4px;
  background: transparent;
}
.form-control::placeholder {
  color: $color-background;
}

.btn-primary {
  background-color: #014c87;
  border-color: #007bff;
  margin-top: 1rem;
  width: 100%;

  &:hover {
    background-color: #0056b3;
    border-color: #004080;
  }
}
.duvidas {
  background-color: $color-primary;
  color: $color-background;
  padding: 1rem 0 0 0;

  h3 {
    font-size: 1.2rem;
  }
}
.row {
 
}
.card {
  border: none;
  background: transparent;
  padding: 10px;
  color: $color-background;
  width: 100%; 

  .card-title {
    font-size: 15px;
    margin: 0.1rem 0 0.3rem 0;
  }

  .card-text {
    font-size: 24px;
    margin-bottom: 0;
  }
  .card-body{
    margin: 20px;
  }
  .card-body img {
    width: 1rem;
  }
  .card-body a {
    color: $color-background;
  }
  .card-body p {
    font-size: 12px;
  }
  .redes-sociais a {
    margin-right: 5px;
  }
}
.whatsapp {
  background-color: $color-secondary;
}


</style>
