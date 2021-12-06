<template>
  <div class="w-full border-2 px-8 py-10 rounded-lg mt-14">
    <div class="w-full flex items-center justify-between mb-7">
      <h3 class="font-bold text-xl text-black">{{ stand.name }}</h3>
      <p class="text-moderate-cyan">Pledge {{ stand.min_price }} or more</p>
    </div>
    <p class="text-dark-gray text-justify">{{ stand.description }}</p>
    <div class="w-full flex items-center justify-between mt-7">
      <!-- left -->
      <div class="flex items-center justify-center">
        <span class="text-3xl font-bold text-black mr-2">{{ stand.left }}</span>
        <span class="text-base text-dark-gray font-normal">left</span>
      </div>
      <!-- Button reward -->
      <button
        class="py-2 px-6 text-white font-bold bg-moderate-cyan hover:bg-dark-cyan rounded-full transition duration-200"
      @click="handleOpenRewards" >Select reward</button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    stand: { type: Object },
    handleOpenRewards: { type: Function },
  }
}
</script>

<style>
</style>