<template>
  <section class="container">
    <h1 class=" text-center">Nuestros Productos</h1>
    <div class="row">
      <div v-for="carta in cartas" :key="carta.id" class="col-12 col-md-4 px-5 mb-4">
        <Card :id="carta.id" :nombre="carta.nombre" :imagen="carta.imagen" :descripcion="carta.descripcion"
          :precio="carta.precio" :cantidad="carta.cantidad" />
      </div>
    </div>
  </section>
</template>

<script>
import Card from '../components/Card.vue'

export default {
  name: 'Homeview',
  components: {
    Card,
  },
  data() {
    return {
      cartas: [
        {
          id: 1,
          nombre: "Colaciones",
          imagen: "/img/colaciones.jpg",
          descripcion: "Exquisitas colaciones caseras",
          precio: 5000,
          cantidad: "Para 1 persona",
        },
        {
          id: 2,
          nombre: "Bebidas",
          imagen: "/img/bebidas.jpg",
          descripcion: "Refrescantes bebidas, tenemos en lata y en botella",
          precio: 1500,
          cantidad: "Tenemos Promo 2X1",
        },
        {
          id: 3,
          nombre: "Desayunos",
          imagen: "/img/desayunos.jpg",
          descripcion: "Sabrosos desayunos hasta las 11H00",
          precio: 3500,
          cantidad: "Te o Café + Churrasco",
        },
        {
          id: 4,
          nombre: "Dulces",
          imagen: "/img/dulces.jpg",
          descripcion: "Delicioso dulces de La Ligua",
          precio: 2500,
          cantidad: "Caja de 6 Unidades",
        },
        {
          id: 5,
          nombre: "Empanadas",
          imagen: "/img/empanadas.jpg",
          descripcion: "Deliciosas Empanadas de Pino, Napolitana y Champiñon Queso",
          precio: 2000,
          cantidad: "1 Unidad",
        },
        {
          id: 6,
          nombre: "Frutas y Verduras",
          imagen: "/img/verduras.jpg",
          descripcion: "Frutas y Verduras frescas",
          precio: 1500,
          cantidad: "1 Kilo",
        },
      ],
    };
  },
}
</script>