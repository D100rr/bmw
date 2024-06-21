<script setup>
import 'primeicons/primeicons.css';
import myHeader from './components/app/myHeader.vue';
import homeView from './views/HomeView.vue';
</script>

<template>
  <div>
    <my-header/>
    <main class="main">
      <RouterView />
    </main>
  </div>
</template>

<style lang="scss" scoped>

</style>

