<template>
  <div class="importancia-container">
    <!-- Barra de navegación -->
    <NavBar />

    <h1>Importancia de la Fotosíntesis</h1>
    
    <section class="content">
      <div class="text">
        <p>
          La fotosíntesis es un proceso vital para la vida en la Tierra. A través de este proceso, las plantas, las algas y algunas bacterias convierten la luz solar en energía química, creando glucosa y oxígeno a partir del dióxido de carbono y agua. Este proceso no solo proporciona alimento para las plantas, sino que también es fundamental para la supervivencia de casi todos los organismos en nuestro planeta.
        </p>
        <h2>Beneficios de la Fotosíntesis</h2>
        <ul>
          <li><strong>Producción de Oxígeno:</strong> La fotosíntesis genera oxígeno como subproducto, lo que es esencial para la respiración de la mayoría de los seres vivos.</li>
          <li><strong>Base de la Cadena Alimentaria:</strong> Proporciona energía a los herbívoros, que a su vez son consumidos por carnívoros, estableciendo así una base alimentaria para todos los ecosistemas.</li>
          <li><strong>Regulación del Clima:</strong> Ayuda a controlar los niveles de dióxido de carbono en la atmósfera, contribuyendo a mitigar el cambio climático.</li>
          <li><strong>Producción de Recursos:</strong> Los productos de la fotosíntesis, como la glucosa, son utilizados para la producción de biomasa, que se convierte en alimentos, biocombustibles y otros recursos útiles.</li>
        </ul>
        <h2>Importancia Ecológica y Económica</h2>
        <p>
          La fotosíntesis no solo es crucial para el equilibrio ecológico, sino que también tiene un impacto económico significativo. La agricultura depende de las plantas fotosintéticas para producir alimentos y materias primas. Sin la fotosíntesis, la vida tal como la conocemos no podría existir.
        </p>
        <p>
          Además, la investigación sobre la fotosíntesis ha llevado al desarrollo de tecnologías sostenibles, como paneles solares inspirados en el proceso natural de conversión de luz en energía.
        </p>
      </div>

      <!-- Imagen representativa de la importancia -->
      <div class="image-container">
        <img src="https://media.istockphoto.com/id/1571993866/es/foto/cultivo-de-plantas-con-rayos-de-sol.jpg?s=612x612&w=0&k=20&c=rlf8FePLVKyxvpRd_Gj4VHacmJZNz4qDvXx_4knG-Bk=" alt="Importancia de la Fotosíntesis" />
      </div>
    </section>
  </div>
</template>

<script setup>
import NavBar from '@/components/NavBar.vue'
</script>

<style scoped>
.importancia-container {
  padding: 20px;
  background-color: #e3f2fd;
  font-family: Arial, sans-serif;
  text-align: center;
}

h1 {
  color: #388e3c; /* Verde suave */
  margin-bottom: 20px;
}

h2 {
  color: #1976d2; /* Azul oscuro */
  margin-top: 20px;
  margin-bottom: 10px;
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
  width: 80%;
  height: auto;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  margin-bottom: 20px
}
</style>