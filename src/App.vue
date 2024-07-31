<template>
  <div id="app">
    <Header />
    <Form />
    <Parceiros />
    <Newsletter />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Form from './components/Form.vue';
import Parceiros from './components/Parceiros.vue';
import Newsletter from './components/Newsletter.vue';
import Footer from './components/Footer.vue';
export default {
  name: 'App',
  components: {
    Header,
    Form,
    Parceiros,
    Newsletter,
    Footer
  }
}
</script>
