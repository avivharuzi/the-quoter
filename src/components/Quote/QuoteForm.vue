<template>
  <div class="row justify-content-center">
    <div class="col-md-12">
      <form autocomplete="off" novalidate>
        <label>Quote</label>
        <textarea v-model="quote" rows="3" class="form-control"></textarea>
        <button class="btn btn-success mt-3" @click.prevent="addQuote">Add Quote</button>
      </form>
    </div>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        quote: null
      }
    },
    methods: {
      addQuote () {
        this.$emit('newQuote', this.quote)
        this.quote = null
      }
    }
  }
</script>
