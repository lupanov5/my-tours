<!-- app.vue -->
<template>
  <div>
    <Header /> <!-- Глобальный хедер -->

    <main>
      <div class="wrapper">
        <NuxtPage /> <!-- Контент страниц -->
      </div>
    </main>

    <Footer /> <!-- Глобальный футер -->
  </div>
</template>

<script setup>
import Header from '~/components/Header.vue'
import Footer from '~/components/Footer.vue'
</script>

<style lang="scss">
@use "~/assets/scss/main.scss";
</style>