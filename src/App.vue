<template>
  <div id="app">
    <bad-flower :leafs="leafs"></bad-flower>
  </div>
</template>

<script>
import BadFlower from './components/BadFlower';

export default {
  name: 'app',
  components: {
      BadFlower
  },
    data: function() {
        return {
            leafs : [
                { competence_id: 1,  competence_name: "Бюджетирование и финансовое планирование", score: 2, total: 10, total_correct: "2", percent_correct: 50, percent_min: 50, passed: true },
                { competence_id: 2,  competence_name: "Бюджетирование и финансовое планирование", score: 2, total: 10, total_correct: "2", percent_correct: 60, percent_min: 80, passed: true },
                { competence_id: 3,  competence_name: "Бюджетирование и финансовое планирование", score: 2, total: 10, total_correct: "2", percent_correct: 35, percent_min: 90, passed: false },
                { competence_id: 4,  competence_name: "Бюджетирование и финансовое планирование", score: 2, total: 10, total_correct: "2", percent_correct: 50, percent_min: 30, passed: true },
                { competence_id: 5,  competence_name: "Бюджетирование и финансовое планирование", score: 2, total: 10, total_correct: "2", percent_correct: 45, percent_min: 70, passed: true },
                { competence_id: 6,  competence_name: "Бюджетирование и финансовое планирование", score: 2, total: 10, total_correct: "2", percent_correct: 38, percent_min: 80, passed: true },
                { competence_id: 7,  competence_name: "Бюджетирование и финансовое планирование", score: 2, total: 10, total_correct: "2", percent_correct: 80, percent_min: 60, passed: true },
                { competence_id: 8,  competence_name: "Бюджетирование и финансовое планирование", score: 2, total: 10, total_correct: "2", percent_correct: 60, percent_min: 50, passed: false },
                { competence_id: 9,  competence_name: "Бюджетирование и финансовое планирование", score: 2, total: 10, total_correct: "2", percent_correct: 28, percent_min: 65, passed: true },
                { competence_id: 10, competence_name: "Бюджетирование и финансовое планирование", score: 2, total: 10, total_correct: "2", percent_correct: 74, percent_min: 60, passed: true},
            ]}
    }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
