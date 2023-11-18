<script>
import Button from "primevue/button"
import Dialog from "primevue/dialog"
import PieceTimeLine from '../components/PieceTimeLine.vue';
import { ref } from "vue";

const showAddPieceModal = ref(false);

export default {
  data() {
    return {
      showAddPieceModal
    }
  },
  components: {
    Button,
    PieceTimeLine,
    Dialog
  }
}
</script>

<template>
  <main>
    <h1>Welcome to <span class="colored-title">Dev Steps</span></h1>
    <h2>Leave one piece of advice you wish you had heard from your present self?</h2>
    <div class="buttons-container">
      <Button label="Create piece" rounded outlined @click="showAddPieceModal = true" />
      <Button label="Check my pieces" severity="secondary" rounded outlined />
    </div>
    <PieceTimeLine />
  </main>

  <Dialog v-model:visible="this.showAddPieceModal" modal header="Header" :style="{ width: '50vw'}" style="background-color: #212121;">
    <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
        Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
    </p>
    <template #footer>
        <Button label="No" icon="pi pi-times" @click="showAddPieceModal = false" text />
        <Button label="Yes" icon="pi pi-check" @click="showAddPieceModal = false" autofocus />
    </template>
</Dialog>

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
