<template >
     <nav class="nav-container">
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
        <RouterLink to="/about">About</RouterLink>
        <RouterLink to="/about">About</RouterLink>
        <RouterLink to="/about">About</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
</template>
<script>
import { RouterLink } from 'vue-router'

export default {
    components: {
        RouterLink
    }
}
</script>
<style lang="css">
    .nav-container {
        display: flex;
        justify-content: center;
        gap: 2rem;
    }

    .nav-container a {
        text-decoration: none;
        color: #fff;
        font-weight: bold;
        font-size: 1.5rem;
    }

    .nav-container a:hover {
        color: #ffd900;
    }
</style>
