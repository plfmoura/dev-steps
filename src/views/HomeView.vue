<script>
import Button from "primevue/button"

export default {
  components: {
    Button
  }
}
</script>

<template>
  <main>
    <h1>Welcome to <span class="colored-title">Dev Steps</span></h1>
    <h2>Leave one piece of advice you wish you had heard from your present self?</h2>
    <div class="buttons-container">
      <Button label="Create piece" rounded/>
      <Button label="Check my pieces" severity="secondary" rounded />
    </div>
  </main>
</template>

<style>
.colored-title {
  color: #ffd900;
}

.buttons-container {
  display: flex;
  margin-top: 1rem;
  gap: 1rem;
}
</style>
