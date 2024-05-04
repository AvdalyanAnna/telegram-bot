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

    provide('tg', tg)


</script>

<template>
  <div>
    <div v-if="tg.query_id.query_id">
      <NuxtPage/>
    </div>
    <div v-else>
      Доступ только через Telegram
    </div>

<!--    <pre>{{ tg.initDataUnsafe}}</pre>-->
  </div>
</template>
