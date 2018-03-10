<template>
  <div class="row">
    <form>
      <div class="col-md-4 col-md-offset-4">
        <h3>Add new quote here</h3>
        <textarea rows="4" v-model="quote"></textarea>
      </div>
      <div class="col-md-6 col-md-offset-3">
        <button class="btn btn-primary" @click.prevent="createQuote">add new quote</button>
        <hr>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      quote: ''
    }
  },
  methods: {
    createQuote() {
      this.$emit('quoteWasAdded', this.quote);
      this.quote = '';
    }
  }
}
</script>

<style>
</style>
