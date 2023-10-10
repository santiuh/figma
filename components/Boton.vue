<template>
  <button
    class="rounded-sm text-white px-8 py-2"
    color="white"
    style="background-color: #111b47; border: solid #111b47"
    :style="transparente ? 'background-color: transparent; color: #111b47' : ''"
  >
    {{ texto }}
  </button>
</template>
<script setup>
const props = defineProps(["texto", "transparente"]);
</script>
