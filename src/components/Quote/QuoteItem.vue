<template>
  <div class="col-md-3 mt-5">
    <div class="card quote-item">
      <div class="card-body text-center">
        <slot></slot>
      </div>
    </div>
  </div>
</template>

<style scoped>
  .quote-item {
    transition: background 0.3s ease-in;
  }

  .quote-item:hover {
    background: #ff7979;
    cursor: pointer;
  }
</style>
