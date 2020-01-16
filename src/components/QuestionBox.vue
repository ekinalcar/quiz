<template>
  <div class="question-box-container">
    <b-jumbotron
      header="BootstrapVue"
      lead="Bootstrap v4 Components for Vue.js 2"
    >
      <template v-slot:lead>{{ currentQuestion.question }}</template>
      <hr class="my-4" />
      <p v-for="answer in answers" :key="answer.id">{{ answer }}</p>
      <b-button variant="primary" href="#">Submit</b-button>
      <b-button @click="next" variant="success" href="#">Next</b-button>
    </b-jumbotron>
  </div>
</template>

<script>
export default {
  props: {
    currentQuestion: Object,
    next: Function
  },
  computed: {
    answers() {
      console.log(this.currentQuestion.incorrect_answers);
      let answers = [...this.currentQuestion.incorrect_answers];
      answers.push(this.currentQuestion.correct_answer);
      return answers;
    }
  }
};
</script>
