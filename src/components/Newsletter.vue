<template>
  <div class="newsletter-container">
    <h2 class="newsletter-title">Newsletter</h2>
    <p class="newsletter-subtitle">
      Quer receber nossas dicas e novidades? Cadastre-se agora
    </p>
    <form @submit.prevent="handleSubmit">
      <div class="input-group mb-3">
        <input
          type="email"
          class="form-control"
          placeholder="Digite seu email"
          aria-label="Digite seu email"
          aria-describedby="button-addon2"
          required
        />
      </div>
    </form>
  </div>
</template>

<script>
export default {
  methods: {
    handleSubmit() {
      alert("Inscrição realizada com sucesso!");
    },
  },
};
</script>

<style scoped lang="scss">
@import "@/assets/styles/variables.scss";

.newsletter-container {
  background-color: $color-primary;
  padding: 20px;
  text-align: center;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  color: $color-background;
  width: 100%;
  margin:0 auto;
}

.newsletter-title {
  font-size: 24px;
  margin-bottom: 10px;
}

.newsletter-subtitle {
  font-size: 15px;
  margin-bottom: 20px;
}

.input-group .form-control {
  border: 1px solid white;
  background-color: transparent;
  color: $color-background;
}

.input-group .form-control::placeholder {
  color: rgba(255, 255, 255, 0.6);
}

.btn-primary {
  background-color: #014c87;
  border-color: #007bff;

  &:hover {
    background-color: #0056b3;
    border-color: #004080;
  }
}
</style>
