<template>
  <div class="index-container">
    <!-- Barra de navegación reutilizable -->
    <NavBar />

    <!-- Contenido principal -->
    <h1>Introducción a la Fotosíntesis</h1>

    <section class="content">
      <div class="text">
        <p>
          La fotosíntesis es un proceso fundamental para la vida en la Tierra, ya que es la forma en que las plantas, 
          algas y algunas bacterias convierten la energía de la luz solar en energía química. Este proceso ocurre en los 
          cloroplastos de las células vegetales, donde la luz solar, el agua y el dióxido de carbono se transforman en 
          oxígeno y glucosa, elementos esenciales para el crecimiento y desarrollo de las plantas.
        </p>
        <p>
          A lo largo de este OVA, aprenderás sobre las dos fases principales de la fotosíntesis: la fase luminosa y la fase 
          oscura. También entenderás la importancia de este proceso no solo para las plantas, sino para todo el ecosistema 
          terrestre. La fotosíntesis no solo provee oxígeno a la atmósfera, sino que también es la base de las cadenas alimenticias.
        </p>
      </div>

      <!-- Imagen de la portada -->
      <div class="image-container">
        <img src="https://cloudfront-us-east-1.images.arcpublishing.com/abccolor/4V2JGGEVQZA4NKRBMJGVYLQYMY.jpg" alt="Fotosíntesis" />
      </div>
    </section>
  </div>
</template>

<script setup>
import NavBar from '@/components/NavBar.vue'
</script>

<style scoped>
.index-container {
  padding: 20px;
  background-color: #f0f8ff;
  font-family: Arial, sans-serif;
  text-align: center;
}

h1 {
  color: #2e7d32;
  margin-bottom: 20px;
}

.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 20px;
}

.text {
  max-width: 800px;
  line-height: 1.6;
  font-size: 1.1rem;
  text-align: justify;
}

.image-container {
  display: flex;
  justify-content: center;
  width: 100%;
  max-width: 800px;
}

img {
  width: 100%;
  height: auto;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}
</style>