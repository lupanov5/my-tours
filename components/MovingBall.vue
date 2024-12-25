<template>
  <div class="moving-ball" ref="ball"></div>
</template>

<style scoped>
.moving-ball {
  position: fixed;
  top: 50%; /* Стартовая позиция */
  left: 50%;
  width: 50px; /* Размер шарика */
  height: 50px;
  background: radial-gradient(circle, #ff7f50, #ff4500);
  border-radius: 50%;
  pointer-events: none; /* Не блокирует клики */
  z-index: 100; /* Поверх других элементов */
}
</style>

<script>
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);

export default {
  mounted() {
    const ball = this.$refs.ball;

    // Анимация шарика
    gsap.to(ball, {
      scrollTrigger: {
        trigger: "body", // Анимация на всю страницу
        start: "top top",
        end: "bottom bottom",
        scrub: true, // Связываем с прокруткой
      },
      x: () => window.innerWidth / 2 - 300, // Двигаем шарик по оси X
      y: () => window.innerHeight / 2 - 400, // Двигаем шарик по оси Y
      rotation: 360, // Вращение шарика
      scale: 1.2, // Легкая пульсация
      ease: "power1.inOut",
      motionPath: {
        path: [
          { x: -500, y: -400 },
          { x: 0, y: -300 },
          { x: 200, y: -100 },
          { x: 0, y: 0 },
          { x: -200, y: -100 },
          { x: 0, y: -300 },
          { x: 200, y: -100 },
          { x: 0, y: 0 },
        ],
        autoRotate: false,
      },
    });
  },
};
</script>
