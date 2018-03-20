<template>
  <div class="alert alert-success text-center">
      <h1>that's correct</h1>
      <br>
      <button class="btn btn-primary" @click="onNextQuestion">Next Question</button>
  </div>
</template>

<script>
    export default {
        methods: {
            onNextQuestion() {
                this.$emit('confirmed')
             }
        }
    }
</script>