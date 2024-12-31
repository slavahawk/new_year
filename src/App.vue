<template>
  <div class="landing">
    <header class="header">
      <h1>Вика, с новым годом!</h1>
      <p>
        Этот сайт я сделал специально для тебя, как открытка) <br />
        <br />
        И я хочу поздравить тебя с Новым годом. Обрати внимание, что тут падает
        снежок и убирает каждые
        <span style="text-wrap: nowrap">20 сек </span> машинка😄 <br /><br />

        Ниже мои друзья записали видео! Приятного просмотра) А в самом низу тебя
        ждет подарок!
      </p>
    </header>
    <main class="main-content">
      <video class="video" :src="Video" controls></video>
      <Button
        as="a"
        :href="Video"
        download="IMG_4993.mp4"
        severity="secondary"
        class="download-button"
      >
        Скачать видео
      </Button>
      <p>Если будут проблемы, напиши мне, скину так)</p>
      <h2 class="gift-header">Ниже твой скромный подарочек!</h2>
      <Button @click="checkPassword" severity="secondary" class="gift-button"
        >Забрать подарок
      </Button>
    </main>
  </div>
</template>

<script setup>
import { Button } from "primevue";
import Video from "./assets/IMG_4993.mp4";

function checkPassword() {
  let password = prompt("Введите пароль:");
  let correctPassword = "Вика";

  if (password === correctPassword) {
    window.location.href =
      "https://ga.gift/ru/cb5db3a35f27464fbb15b16967c32ea7";
  } else {
    alert("Неверный пароль");
  }
}
</script>

<style scoped>
.landing {
  margin: 0 auto;
  max-width: 500px;
  color: #1f4f83;
  padding: 20px;
  text-align: center;
}

.header {
  padding: 20px;
  background-color: white;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.header p {
  line-height: 22px;
}

.main-content {
  margin: 20px 0;
}

.video {
  width: 100%;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.download-button,
.gift-button {
  margin-top: 20px;
  margin-bottom: 20px;
}

.gift-header {
  margin-top: 40px;
}
</style>
