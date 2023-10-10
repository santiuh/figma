<template>
  <div class="w-full flex flex-col justify-center">
    <p class="flex justify-center">
      <h4  class="text-4xl text-white">{{
        counter
      }}</h4>
    </p>
    <h2 class="flex justify-center text-lg text-white ">{{ titulo }}</h2>
  </div>
</template>

<script setup>
// let options = {
//   root: document.querySelector("h4"),
//   rootMargin: "0px",
//   threshold: 1.0,
// };

const lala = (e) => {
  if(e[0].intersectionRect.left !== 0 ){
    const counterInterval = setInterval(() => {
  if (counter.value < props.numero) {
    counter.value++;
    counter.value++;
  } else {
    clearInterval(counterInterval);
  }
}, props.intervalo);

  }
  
}



onBeforeMount(() => {


})
onMounted(() => {
  nextTick(() => {  
    let cody = document.querySelector("h4");
    let observer = new IntersectionObserver(lala,{});
    observer.observe(cody)
  })
})




// DIVISOR
const props = defineProps(["numero", "intervalo", "titulo"]);

const counter = ref(0);

</script>
