<template>
  <div class="contenedor-de-resumen">
    <!-- Barra de navegación -->
    <NavBar />

    <h1>Resumen de la Fotosíntesis</h1>
    <p>
      La fotosíntesis es el proceso mediante el cual las plantas, las algas y algunas bacterias convierten la luz solar en energía química, almacenando esta energía en forma de glucosa. Este proceso ocurre principalmente en las hojas de las plantas, que contienen clorofila, el pigmento que les da su color verde y les permite absorber la luz solar.
    </p>
    <p>
      La fotosíntesis se divide en dos fases: la fase luminosa, que requiere luz solar, y la fase oscura, que no la requiere. En la fase luminosa, la energía solar se convierte en energía química en forma de ATP y NADPH, mientras que en la fase oscura, la planta utiliza esta energía química para convertir el dióxido de carbono y el agua en glucosa.
    </p>
    
    <!-- Aquí se llama al componente del examen -->
    <Exam />
  </div>
</template>

<script setup>
import NavBar from '@/components/NavBar.vue';
</script>

<style scoped>
.contenedor-de-resumen {
  padding: 20px;
  background-color: #f0f8ff; /* Fondo coherente con las otras páginas */
  font-family: Arial, sans-serif;
  text-align: left
}

h1 {
  color: #388e3c; /* Color verde para el título */
  margin-bottom: 20px;
  text-align: center;
}

p {
  margin: 10px 0;
}
</style>