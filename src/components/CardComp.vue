<template>
    <div class="card">
      <slot name="cardTitle"></slot>
      <slot name="cardContent"></slot>
    </div>
</template>

<script>

</script>
  
  <style>
  .card {
  border: 1px solid #ccc;
  padding: 10px;
  margin: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
  </style>