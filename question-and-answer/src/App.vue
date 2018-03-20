<template>
  <div id="app">
    <div class="container">
      <div class="row">
        <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-lg-6 col-lg-offset-3">
          <h1 class="text-center">question and answer quest</h1>
        </div>
      </div>
      <div class="row">
        <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-lg-6 col-lg-offset-3">
          <component :is="mode" @answered="answered($event)" @confirmed=" mode = 'app-question' "></component>  
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Question from './components/Question.vue';
import Answer from './components/Answer.vue';

export default {
  data() {
    return {
          mode: 'app-question'
    }
  },
  methods: {
    answered(isCorrect) {
      if(isCorrect) {
        this.mode = 'app-answer'
      } else {
        this.mode = 'app-question';
        alert('sorry! try again');
      }
    }
  },
  components: {
    appQuestion: Question,
    appAnswer: Answer
  }
}

</script>

<style>

</style>
