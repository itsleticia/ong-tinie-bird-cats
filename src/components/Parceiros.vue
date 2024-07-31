<template>
  <div class="parceiros">
    <h2>Nossos Parceiros</h2>
    <div class="parceiros-logos">
      <img src="@/assets/images/petlove.png" alt="Petlove" class="parceiro-logo">
      <img src="@/assets/images/golden.png" alt="Golden" class="parceiro-logo">
      <img src="@/assets/images/whiskas.png" alt="Whiskas" class="parceiro-logo">
      <img src="@/assets/images/royal.png" alt="Royal Canin" class="parceiro-logo">
      <img src="@/assets/images/premier.png" alt="Premier pet" class="parceiro-logo">
    </div>
  </div>
</template>

<script>
export default {
  name: 'Parceiros',
};
</script>

<style scoped lang="scss">
@import "@/assets/styles/variables.scss";

.parceiros {
  text-align: center;
  padding: 20px;
  background-color: #ffffff;
}

.parceiros-logos {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  gap: 20px;
  margin-bottom: 2rem;

}
h2{
    font-size:1rem;
    margin: 2rem 0;
}
  
.parceiro-logo {
    max-width: 100px; 
    height: auto;
    object-fit: contain;
}


</style>
