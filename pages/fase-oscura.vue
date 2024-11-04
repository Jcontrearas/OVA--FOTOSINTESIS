<template>
  <div class="fase-oscura-container">
    <!-- Barra de navegación -->
    <NavBar />

    <h1>Fase Oscura de la Fotosíntesis</h1>
    
    <section class="content">
      <div class="text">
        <p>
          La fase oscura, también conocida como el ciclo de Calvin, es una parte crucial del proceso de la fotosíntesis que no requiere luz directa para llevarse a cabo. Este ciclo ocurre en el estroma de los cloroplastos y se basa en la utilización del ATP y NADPH generados durante la fase luminosa.
        </p>
        <p>
          Durante la fase oscura, el dióxido de carbono (CO<sub>2</sub>) es capturado de la atmósfera y, a través de una serie de reacciones químicas, se convierte en glucosa. Este proceso es esencial para la producción de energía en las plantas y permite la creación de compuestos orgánicos que servirán como fuente de energía para otros organismos en la cadena alimentaria.
        </p>
        <p>
          En términos simples, la fase oscura se puede resumir en los siguientes pasos:
        </p>
        <ol>
          <li>Fijación del CO<sub>2</sub>: El dióxido de carbono se une a una molécula de cinco carbonos llamada ribulosa bifosfato (RuBP).</li>
          <li>Reducción: Los compuestos resultantes son convertidos en gliceraldehído-3-fosfato (G3P) utilizando la energía del ATP y NADPH.</li>
          <li>Regeneración: Parte del G3P se utiliza para regenerar RuBP, permitiendo que el ciclo continúe.</li>
          <li>Producción de glucosa: Finalmente, dos moléculas de G3P se combinan para formar una molécula de glucosa.</li>
        </ol>
        <p>
          Este proceso es vital no solo para las plantas, sino también para todos los seres vivos, ya que la glucosa generada se utiliza como fuente de energía por muchos organismos, incluidos los humanos.
        </p>
      </div>

      <!-- Imagen representativa de la fase oscura -->
      <div class="image-container">
        <img src="https://i.ytimg.com/vi/mqNaJahbQ0k/maxresdefault.jpg" alt="Fase Oscura" />
      </div>
    </section>
  </div>
</template>

<script setup>
import NavBar from '@/components/NavBar.vue'
</script>

<style scoped>
.fase-oscura-container {
  padding: 20px;
  background-color: #f0f8ff;
  font-family: Arial, sans-serif;
  text-align: center;
}

h1 {
  color: #388e3c; /* Verde suave */
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