<template>
  <div class="exam-container">
    <h1>Examen de Conocimientos sobre la Fotosíntesis</h1>

    <form @submit.prevent="checkAnswers" v-if="!isSubmitted">
      <div class="question" v-for="(question, index) in questions" :key="index">
        <p>{{ question.text }}</p>
        <div class="options">
          <label v-for="(option, optIndex) in question.options" :key="optIndex" class="option-label">
            <input type="checkbox" :value="option" v-model="selectedAnswers[index]" />
            {{ option }}
          </label>
        </div>
      </div>

      <button type="submit" class="submit-btn">Enviar respuestas</button>
    </form>

    <div v-if="isSubmitted" class="results-container">
      <h2>Tu nota: {{ score }}</h2>
      <div class="feedback-message" :class="getFeedbackClass">
        {{ getFeedbackMessage }}
      </div>
      <button @click="resetExam" class="reset-btn">Reiniciar examen</button>
    </div>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue';

const questions = [
  {
    text: "1. ¿Cuál de los siguientes gases utilizan las plantas durante la fotosíntesis?",
    options: ["Oxígeno", "Dióxido de carbono", "Nitrógeno", "Helio"],
    answers: ["Dióxido de carbono"]
  },
  {
    text: "2. ¿Qué producen las plantas durante la fase luminosa?",
    options: ["Glucosa", "Agua", "Oxígeno", "Calor"],
    answers: ["Oxígeno"]
  },
  {
    text: "3. ¿Qué fase de la fotosíntesis utiliza la luz del sol?",
    options: ["Fase oscura", "Fase luminosa", "Fase líquida", "Fase gaseosa"],
    answers: ["Fase luminosa"]
  },
  {
    text: "4. ¿Para qué utilizan las plantas la glucosa que producen?",
    options: ["Como aire", "Como alimento", "Como sombra", "Como perfume"],
    answers: ["Como alimento"]
  },
  {
    text: "5. ¿Cuál es la importancia del oxígeno producido por las plantas?",
    options: ["No tiene importancia", "Es vital para los animales y humanos", "Solo lo usan las plantas", "Es dañino"],
    answers: ["Es vital para los animales y humanos"]
  }
];

const selectedAnswers = ref(Array(questions.length).fill([]));
const score = ref(null);
const isSubmitted = ref(false);

const getFeedbackMessage = computed(() => {
  const scoreNum = parseFloat(score.value);
  if (scoreNum === 5) return "¡Excelente! Has dominado el tema de la fotosíntesis.";
  if (scoreNum >= 4) return "¡Muy bien! Casi perfecto.";
  if (scoreNum >= 3) return "Bien, pero aún hay espacio para mejorar.";
  return "Te recomiendo repasar el tema de la fotosíntesis.";
});

const getFeedbackClass = computed(() => {
  const scoreNum = parseFloat(score.value);
  if (scoreNum >= 4) return 'feedback-excellent';
  if (scoreNum >= 3) return 'feedback-good';
  return 'feedback-needs-improvement';
});

const checkAnswers = () => {
  let correctCount = 0;

  selectedAnswers.value.forEach((answers, index) => {
    const correctAnswers = questions[index].answers;
    const isCorrect = correctAnswers.every(answer => answers.includes(answer)) &&
                     correctAnswers.length === answers.length;

    if (isCorrect) {
      correctCount++;
    }
  });

  score.value = ((correctCount / questions.length) * 5).toFixed(2);
  isSubmitted.value = true;
};

const resetExam = () => {
  selectedAnswers.value = Array(questions.length).fill([]);
  score.value = null;
  isSubmitted.value = false;
};
</script>

<style scoped>
.exam-container {
  padding: 20px;
  background-color: #fff;
  font-family: Arial, sans-serif;
  text-align: center;
  border-radius: 20px;
  max-width: 800px;
  margin: 0 auto;
}

h1 {
  color: #388e3c;
  margin-bottom: 20px;
}

.question {
  margin: 20px 0;
  text-align: left;
  font-weight: 700;
  padding: 15px;
  background-color: #f5f5f5;
  border-radius: 10px;
}

.options {
  margin-top: 10px;
  margin-left: 20px;
  font-weight: normal;
}

.option-label {
  display: block;
  margin-bottom: 10px;
  cursor: pointer;
  transition: all 0.2s ease;
  padding: 8px;
}

.option-label:hover {
  background-color: #e8f5e9;
  border-radius: 5px;
}

input[type="checkbox"] {
  margin-right: 10px;
}

.submit-btn, .reset-btn {
  padding: 12px 24px;
  font-size: 16px;
  border: none;
  border-radius: 10px;
  cursor: pointer;
  transition: all 0.3s ease;
  margin: 20px 0;
}

.submit-btn {
  background-color: #388e3c;
  color: white;
}

.reset-btn {
  background-color: #1976d2;
  color: white;
}

.submit-btn:hover, .reset-btn:hover {
  transform: scale(1.05);
  box-shadow: 0 2px 8px rgba(0,0,0,0.2);
}

.results-container {
  padding: 20px;
  margin-top: 20px;
  background-color: #f5f5f5;
  border-radius: 10px;
}

h2 {
  margin-top: 20px;
  color: #1976d2;
  font-size: 24px;
}

.feedback-message {
  margin: 20px 0;
  padding: 15px;
  border-radius: 8px;
  font-size: 18px;
}

.feedback-excellent {
  background-color: #e8f5e9;
  color: #2e7d32;
}

.feedback-good {
  background-color: #fff3e0;
  color: #f57c00;
}

.feedback-needs-improvement {
  background-color: #ffebee;
  color: #c62828;
}
</style>
