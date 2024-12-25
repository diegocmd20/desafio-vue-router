<template>
    <div class="container p-5">
        <div class="card">
            <img :src="carta.imagen" class="card-img-top" :alt="carta.nombre" />
            <div class="card-body">
                <h5 class="card-title fw-bold">{{ carta.nombre }}</h5>
                <p class="card-text">{{ carta.descripcion }}</p>
            </div>
            <ul class="list-group list-group-flush">
                <li class="list-group-item">Precio: $ {{ carta.precio }}</li>
                <li class="list-group-item">Cantidad: {{ carta.cantidad }}</li>
            </ul>
            <div class="card-body">
                <router-link to="/" class="card-link">Ir a Home</router-link>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ProductsView',
    props: ['id'],
    data() {
        return {
            carta: {
                id: 0,
                nombre: '',
                imagen: '',
                descripcion: '',
                precio: 0,
                cantidad: '',
            },
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
            ]
        };
    },
    mounted() {
        if (this.id) {
            this.carta = this.cartas.find((carta) => carta.id === parseInt(this.id));
        }
    }
};
</script>

<style scoped></style>