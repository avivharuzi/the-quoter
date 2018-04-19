<template>
  <div class="row">
    <div class="col-md-12">
      <div class="progress mb-3">
        <div class="progress-bar bg-warning" :style="{ width: (quoteCount / maxQuotes) * 100 + '%' }">
          {{ quoteCount }} / {{ maxQuotes }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    props: {
      quoteCount: Number,
      maxQuotes: Number
    }
  };
</script>
