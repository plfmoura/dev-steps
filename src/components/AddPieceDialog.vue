<template>
    <Dialog :visible="show" modal header="Header" :style="{ width: '50vw' }">
        <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore
            magna
            aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
            consequat.
            Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur
            sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
        </p>
        <template #footer>
            <Button label="No" icon="pi pi-times" @click="show = false" text />
            <Button label="Yes" icon="pi pi-check" @click="show = false" autofocus />
        </template>
    </Dialog>
</template>
<script>
import Dialog from 'primevue/dialog';
import Button from 'primevue/button';

export default {
    props: {
        show: {
            type: Boolean,
            required: true
        }
    },
    components: {
        Dialog,
        Button
    }
}
</script>
<style ></style>