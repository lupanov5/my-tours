<template>
  <header class="header">
    <div class="container">
      <div class="logo">
        <a href="/">MyTours</a>
      </div>
      <nav class="nav">
        <ul>
          <li><a href="/">Главная</a></li>
          <li><a href="/tours">Туры</a></li>
          <li><a href="/contact">Контакты</a></li>
        </ul>
      </nav>
      <div class="cta-button">
        <a href="/signup" class="button">Записаться</a>
      </div>
    </div>
  </header>
</template>

<script setup>
// Логика хедера, если потребуется, может быть добавлена здесь
</script>

<style scoped lang="scss">
@use '~/assets/styles/variables' as *;

// Основной стиль хедера
.header {
  background-color: rgba($primary-color, 0.1); /* Прозрачный фон */
  color: #000; /* Черный текст */
  padding: 15px 0; /* Отступы */
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 100;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1); /* Тень */
  border-radius: 10px; /* Закругленные углы */
  width: 100%;
  margin: 0 auto;
  transition: background-color 0.3s ease; /* Плавное изменение фона */
}

.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: $max-width;
  margin: 0 auto; /* Центрирование */
  padding: 0 20px;
}

// Стили для логотипа
.logo a {
  font-size: 1.8rem;
  font-weight: bold;
  text-decoration: none;
  color: #000; /* Черный цвет текста */
}

// Стили для навигации
.nav ul {
  list-style: none;
  display: flex;
  gap: 2rem;
}

.nav li a {
  text-decoration: none;
  color: #000; /* Черный цвет текста */
  font-size: 1.1rem;
  font-family: $header-font;
  padding: 0.5rem 0;
  position: relative;
  transition: color 0.3s ease;
}

.nav li a:hover {
  color: $secondary-color; /* Цвет при наведении */
}

.nav li a::after {
  content: '';
  position: absolute;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 2px;
  background-color: $secondary-color; /* Подчеркивание */
  transform: scaleX(0);
  transform-origin: bottom right;
  transition: transform 0.3s ease;
}

.nav li a:hover::after {
  transform: scaleX(1);
  transform-origin: bottom left;
}

// Стили для кнопки CTA
.cta-button {
  display: flex;
  justify-content: center;
  align-items: center;
}

// Стили кнопки
.button {
  text-decoration: none;
  background-color: transparent;
  border: 2px solid $secondary-color;
  padding: 10px 20px;
  font-size: 1rem;
  font-family: $header-font;
  color: $secondary-color;
  border-radius: 50px;
  transition: background-color 0.3s, color 0.3s;
}

.button:hover {
  background-color: $secondary-color;
  color: #fff;
}
</style>