<script>
import { RouterView } from 'vue-router'
import Navbar from './components/Navbar.vue'
import Footer from './components/Footer.vue'
import MediosPago from './components/MediosPago.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    Footer,
    MediosPago
  }
}
</script>

<template>
  <Navbar />
  <RouterView />
  <MediosPago />
  <Footer />

</template>

<style scoped></style>
