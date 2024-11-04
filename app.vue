<template>
  <div id="app">
    <header>
      <h1>la Fotosíntesis</h1>
    </header>

    <!-- Aquí se renderizarán las páginas individuales -->
    <NuxtPage />

    <footer>
      <p><footer>
        <footer>
    &copy; 2024 OVA sobre Fotosíntesis. Todos los derechos reservados. Este sitio web fue creado con fines educativos para explicar el proceso de la fotosíntesis. <br>El contenido no puede ser reproducido sin autorización.</br>
</footer>

</footer>
</p>
    </footer>
  </div>
</template>

<script setup>
// No se necesita script aquí a menos que quieras agregar alguna lógica global
</script>

<style scoped>
/* Estilos para todo el sitio */
#app {
  font-family: Arial, sans-serif;
  text-align: center;
  background-color: #f5f5f5;
  padding: 20px;
  overflow-x: hidden
}

header {
  background-color: #4CAF50;
  color: white;
  padding: 20px;
  margin-bottom: 20px;
  border-radius: 10px;
}

footer {
  background-color: #333;
  color: white;
  padding: 10px;
  bottom: 0;
  width: 100%;
}

h1 {
  margin: 0;
  font-size: 2rem;
  text-transform: uppercase;
  text-shadow: 0px 0px 3px #fff;
}

footer p {
  margin: 0;
}
</style>