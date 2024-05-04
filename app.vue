<script setup>

useHead({
  script: [
    {
      src:'https://telegram.org/js/telegram-web-app.js',
    }
  ]
})

const tg = window?.Telegram.WebApp


</script>

<template>
  <div>
    <pre>{{ tg.initDataUnsafe}}</pre>
  </div>
</template>
