<template>
  <div class="p-12 bg-white border-1 rounded-lg">
    <div class="flex items-center w-full text-black">
      <div class="w-1/3 flex flex-col">
        <span class="font-bold text-2xl">$189,914</span>
        <span class="text-base text-dark-gray">of 1100,000 backed</span>
      </div>
      <div class="w-1/3 flex flex-col justify-center items-center border-l-2 border-r-2">
        <span class="font-bold text-2xl">289,914</span>
        <span class="text-base text-dark-gray">total backers</span>
      </div>
      <div class="w-1/3 flex flex-col pl-16">
        <span class="font-bold text-2xl">60</span>
        <span class="text-base text-dark-gray">days left</span>
      </div>
    </div>
    <!-- Progress bar -->
    <div class="rounded-full h-3.5 mt-10 bg-gray-200">
      <div class="rounded-full h-full w-9/12 bg-dark-cyan"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Backers',
}
</script>

<style>
</style>