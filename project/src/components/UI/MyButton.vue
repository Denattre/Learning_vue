<template>
  <button class="btn">
    <slot></slot>
  </button>
</template>

<script>
  export default {
    name: 'my-button'
  }
</script>

<style scoped>
.btn {
    margin-top: 15px;
    padding: 10px;
    background: none;
    color: green;
    border: 1px solid green;
  }
</style>