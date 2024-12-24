<template>
    <div class="container p-5">
        <h1 class="display-3">Escribenos</h1>
        <div class="mb-3">
            <label for="name" class="form-label">Nombre</label>
            <input type="text" class="form-control" id="name" placeholder="Escribe tu nombre">
        </div>
        <div class="mb-3">
            <label for="email" class="form-label">Email</label>
            <input type="email" class="form-control" id="email" placeholder="Escribe tu e-mail aquí">
        </div>
        <div class="mb-3">
            <label for="mensaje" class="form-label">Mensaje</label>
            <textarea class="form-control" id="mensaje" rows="3" placeholder="Escribe tu mensaje aquí"></textarea>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ContactView',
    data() {
        return {};
    }
};
</script>

<style scoped></style>