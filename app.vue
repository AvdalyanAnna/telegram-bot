<script setup>

useHead({
  script: [
    {
      src:'https://telegram.org/js/telegram-web-app.js',
    }
  ]
})

const tg = window?.Telegram.WebApp
// Use SSR-safe IDs for Headless UI
provideHeadlessUseId(() => useId())

</script>

<template>
  <div>
    <NuxtPage/>

<!--    <pre>{{ tg.initDataUnsafe}}</pre>-->
  </div>
</template>
