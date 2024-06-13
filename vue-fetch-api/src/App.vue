<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HomeView from './views/HomeView.vue';
</script>

<template>
  <div>
    <!-- <RouterView /> -->
    <Suspense>
      <template #default>
        <HomeView />
      </template>
      <template #fallback>
        <p>Loading....</p>
      </template>
    </Suspense>

</div>
</template>

<style scoped>

</style>
