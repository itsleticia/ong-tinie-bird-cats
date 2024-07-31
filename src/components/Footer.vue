<template>
  <footer class="footer">
    <div class="container">
      <div class="row align-items-center">
        <!-- Logo -->
        <div class="col-md-4">
          <img src="@/assets/images/logo.png" alt="Logo" class="logo">
          <img src="@/assets/images/logo-footer.png" alt="Logo" class="logo logo-footer">
        </div>
        <!-- Menu -->
        <nav class="col-md-8 text-end">
          <ul class="footer-menu">
            <li><a href="#">Home</a></li>
            <li><a href="#">Sobre</a></li>
            <li><a href="#">Quero Ajudar</a></li>
            <li><a href="#">Notícias</a></li>
            <li><a href="#">Contato</a></li>
          </ul>
        </nav>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
};
</script>

<style scoped lang="scss">
@import '@/assets/styles/variables.scss';

.footer {
  background-color: $color-background;
  padding: 20px 0;
}

.logo {
  max-width: 150px;
}
  .logo-footer{
    margin-left: 0.5rem;
  }

.footer-menu {
  list-style: none;
  display: flex;
  justify-content: flex-end;
  margin: 0;
  padding: 0;

  li {
    margin: 0 15px;
    
}
}



.footer-menu a {
  text-decoration: none;
  color: $color-text;
  &:hover {
    text-decoration: none;
  }
}
</style>
