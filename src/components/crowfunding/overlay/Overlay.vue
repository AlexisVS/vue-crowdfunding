<template>
  <div
    class="w-full overlay min-h-screen bg-black bg-opacity-30 fixed top-0 m-0 left-0 z-50 flex justify-center items-center"
  >
    <div class="rounded-lg p-10 bg-gray-100 flex flex-col justify-center items-center relative">
      <!-- Thanks for your support -->
      <!-- <div class="h-full w-96 font-medium flex flex-col justify-center items-center">
        <img src="../../../assets/icon-check.svg" alt="" class="mb-3">
        <h2 class="font-bold text-lg text-black my-4">Thanks for your support!</h2>
        <p class="text-sm text-dark-gray text-center mb-8 leading-7">Your pledge brings us one step closer to sharing Mastercraft Bamboo Monitor Riser worldwide. You will get an email once our campaign is completed.</p>
        <button class="py-2 px-4 bg-moderate-cyan hover:bg-dark-cyan text-white font-medium rounded-full">Get it!</button>
      </div>-->
      <!-- Back this project -->
      <div class="w-xsl w-overlay">
        <svg class="absolute top-5 right-5 fill-current text-black cursor-pointer" fill="black" width="15" height="15" xmlns="http://www.w3.org/2000/svg"><path d="M11.314 0l2.828 2.828L9.9 7.071l4.243 4.243-2.828 2.828L7.07 9.9l-4.243 4.243L0 11.314 4.242 7.07 0 2.828 2.828 0l4.243 4.242L11.314 0z" fill="currentColor"/></svg>
        <h2 class="font-bold mt-2 text-xl text-black">Back this project</h2>
        <p
          class="text-dark-gray text-xs my-5"
        >Wan to support us in bringing Mastercraft Bamboo Monitor Riser out in the world?</p>
        <Stand />
      </div>
    </div>
  </div>
</template>

<script>
import Stand from "./Stand.vue";
export default {
  name: "Overlay",
  components: { Stand }
}
</script>

<style scoped>
.overlay {
  margin: 0 !important;
}
.w-overlay {
  width: 500px
}
</style>