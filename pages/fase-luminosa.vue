<template>
  <div class="fase-luminosa-container">
    <!-- Navegación mejorada -->
    <nav class="navigation">
      <NuxtLink to="/">Introducción</NuxtLink>
      <NuxtLink to="/fase-luminosa">Fase Luminosa</NuxtLink>
      <NuxtLink to="/fase-oscura">Fase Oscura</NuxtLink>
      <NuxtLink to="/importancia">Importancia</NuxtLink>
      <NuxtLink to="/resumen">Resumen</NuxtLink>
    </nav>

    <h1>Fase Luminosa de la Fotosíntesis</h1>
    
    <section class="content">
      <div class="text">
        <p>
          La fase luminosa es la primera etapa de la fotosíntesis, en la que se requiere luz para que las plantas 
          capturen la energía solar. Este proceso ocurre en los tilacoides de los cloroplastos, donde la energía lumínica 
          se convierte en energía química en forma de ATP y NADPH. Estos productos son esenciales para la siguiente fase 
          de la fotosíntesis, el ciclo de Calvin (o fase oscura).
        </p>
        <p>
          Durante la fase luminosa, las moléculas de agua se dividen en oxígeno, protones y electrones a través de un proceso 
          conocido como fotólisis del agua. El oxígeno liberado es un subproducto vital para la vida en la Tierra, mientras 
          que los protones y electrones son utilizados para generar energía.
        </p>
      </div>

      <div class="image-container">
        <img src="https://www.lifeder.com/wp-content/uploads/2018/12/fase-luminosa-fotosintesis.jpg" alt="Fase luminosa de la fotosíntesis" />
      </div>
    </section>
  </div>
</template>

<style scoped>
.fase-luminosa-container {
  padding: 20px;
  background-color: #f0f8ff;
  font-family: Arial, sans-serif;
}

/* Estilos de navegación */
.navigation {
  display: flex;
  justify-content: center;
  background-color: #4CAF50;
  padding: 15px;
  margin-bottom: 20px;
  border-radius: 5px;
}

.navigation a {
  color: white;
  text-decoration: none;
  margin: 0 15px;
  font-weight: bold;
}

.navigation a:hover {
  transform: scale(1.3);
}

h1 {
  text-align: center;
  margin-bottom: 20px;
  color: #2e7d32;
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
  max-width: 900px;
}

img {
  width: 100%;
  height: auto;
  border-radius: 10px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
  margin-bottom: 30px;
}
</style>