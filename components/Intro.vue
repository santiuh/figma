<template>
  <div
    class="flex flex-col lg:flex-row justify-around items-center my-28 lg:px-0 px-3"
    style="max-height: 569px"
    data-aos="zoom-in"
  >
    <div>
      <img :src="imagen" class="lg:h-80" />
    </div>
    <div>
      <h2
        class="text-secondary text-4xl lg:text-start text-center lg:mt-0 mt-2 mb-3"
      >
        {{ titulo }}
      </h2>
      <p class="text-primary lg:text-start text-center max-w-md">
        Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo
        ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis
        dis parturient montes, nascetur ridiculus mus. Donec quam felis,
        ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa
        quis enim.
      </p>
      <div class="flex justify-end lg:flex-none lg:justify-start">
        <boton class="mt-5" v-if="texto" :texto="texto"></boton>
      </div>
    </div>
  </div>
</template>
<script setup>
const props = defineProps(["titulo", "imagen", "texto"]);
import AOS from "aos";

onMounted(() => {
  AOS.init();
});
</script>
