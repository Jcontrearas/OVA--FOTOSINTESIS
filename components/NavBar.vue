<template>
  <nav class="navigation">
    <NuxtLink to="/" exact>Introducción</NuxtLink>
    <NuxtLink to="/fase-luminosa">Fase Luminosa</NuxtLink>
    <NuxtLink to="/fase-oscura">Fase Oscura</NuxtLink>
    <NuxtLink to="/importancia">Importancia</NuxtLink>
    <NuxtLink to="/resumen">Resumen</NuxtLink>
  </nav>
</template>

<script setup>
// No se necesita lógica en el script para este componente.
</script>

<style scoped>
.navigation {
  display: flex;
  justify-content: center;
  background-color: #4CAF50;
  padding: 15px;
  margin-bottom: 20px;
  border-radius: 10px;
}

.navigation a {
  color: white;
  text-decoration: none;
  margin: 0 15px;
  font-weight: bold;
  transition: transform 0.2s ease-in-out; /* Animación suave */
}

.navigation a:hover {
  transform: scale(1.3); /* Agranda el enlace al pasar el cursor */
}

.navigation a.exact-active {
  text-decoration: underline;
}
</style>
