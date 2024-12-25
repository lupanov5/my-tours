<!-- components/Footer.vue -->
<template>
  <footer class="footer">
    <div class="footer-content">
      <p>&copy; 2024 MyTours. Все права защищены.</p>
    </div>
  </footer>
</template>

<script setup>
// Логика футера (если потребуется) может быть добавлена сюда
</script>

<style scoped lang="scss">

.footer {
  background-color: $footer-background;
  color: #fff;
  text-align: center;
  padding: $padding;
  position: fixed;
  bottom: 0;
  width: 100%;
}

.footer-content p {
  margin: 0;
  font-size: 0.9rem;
  font-family: $base-font;
}
</style>