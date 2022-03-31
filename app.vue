<script setup lang="ts">
  import EVOlogo1 from "./components/EVOlogo1.vue"
  import EVOlogo2 from "./components/EVOlogo2.vue"
  import EVOlogo3 from "./components/EVOlogo3.vue"
</script>
<template>
  <div class="container">
    <EVOlogo2/>
    <EVOlogo3/>
    <EVOlogo1/>
  </div>
</template>

<style scoped>
.container {
  /*width: 100%;*/
  display: grid;
  grid-template-rows: repeat(3, 200px);
  grid-auto-columns: 1fr;
  justify-content: start;
  gap: 40px;
}
</style>
