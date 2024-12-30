<template>
  <div class="landing">
    <header class="header">
      <h1>Вика, с новым годом!</h1>
      <p>
        Этот сайт персонально для тебя и хочется поздравить тебя с новым годом,
        ниже мои друзья записали тебе видео)
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
      <p>
        Если будут проблемы,
        <a href="https://t.me/slavahawk" target="_blank">напиши мне</a>, скину
        так)
      </p>
      <h2 class="gift-header">Ниже твой скромный подарочек!</h2>
      <Button
        as="a"
        href="https://ga.gift/ru/cb5db3a35f27464fbb15b16967c32ea7"
        target="_blank"
        severity="secondary"
        class="gift-button"
        >Забрать подарок
      </Button>
    </main>
  </div>
</template>

<script setup>
import { Button } from "primevue";
import Video from "./assets/IMG_4993.mp4";
</script>

<style scoped>
.landing {
  color: #1f4f83;
  padding: 20px;
  text-align: center;
}

.header {
  padding: 20px;
  background-color: #ffcccc;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
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
