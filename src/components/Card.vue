<template>
  <div class="card">
    <img :src="imagen" class="card-img-top" :alt="nombre" />
    <div class="card-body">
      <h5 class="card-title fw-bold">{{ nombre }}</h5>
      <p class="card-text">{{ descripcion }}</p>
    </div>
    <ul class="list-group list-group-flush">
      <li class="list-group-item">Precio: $ {{ precio }}</li>
      <li class="list-group-item">Cantidad: {{ cantidad }}</li>
    </ul>
    <div class="card-body">
      <router-link :to="`/productos/${id}`" class="card-link">Ver más</router-link>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Card',
  props: {
    id: {
      type: Number,
      required: true,
    },
    nombre: {
      type: String,
      required: true,
    },
    imagen: {
      type: String,
      required: true,
    },
    descripcion: {
      type: String,
      required: true,
    },
    precio: {
      type: Number,
      required: true,
    },
    cantidad: {
      type: String,
      required: true,
    },
  }
}
</script>
<style></style>