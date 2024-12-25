<!-- app.vue -->
<template>
  <div>
    <Header /> <!-- Глобальный хедер -->
    <main>
      <NuxtPage /> <!-- Контент страниц -->
    </main>
    <Footer /> <!-- Глобальный футер -->
  </div>
</template>

<script setup>
import Header from '~/components/Header.vue'
import Footer from '~/components/Footer.vue'
</script>

<style scoped>
/* Глобальные стили можно поместить сюда */
main {
  margin-top: 80px; /* Отступ для хедера */
  margin-bottom: 60px; /* Отступ для футера, чтобы он не перекрывал контент */
}
</style>