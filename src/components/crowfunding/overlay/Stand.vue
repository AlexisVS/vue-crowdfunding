<template>
  <div class="border-2 border-gray-300 rounded-lg flex py-6" @click="handleStandSelect(stand.id);">
    <div class="w-16 flex justify-center">
      <input
        type="radio"
        class="bg-gray-100 border-0 mt-0.5 ring-2 ring-dark-cyan caret-dark-cyan text-dark-cyan"
        name="inputRadioOverlayStand"
        v-model="standSelected"
        :value="stand.id"
        @click="handleStandSelect(stand.id)"
      />
    </div>
    <div class="w-full pr-4">
      <div class="w-full mb-6 flex items-center justify-between">
        <div class="flex justify-between space-x-4">
          <h3 class="text-black hover:text-dark-cyan font-bold">{{ stand.name }}</h3>
          <h3 class="text-dark-cyan font-semibold">Pledge ${{ stand.min_price }} or more</h3>
        </div>
        <div class="flex items-center">
          <span class="font-bold text-black">{{ stand.left }}</span>
          <span class="text-base text-dark-gray ml-2.5">left</span>
        </div>
      </div>
      <p class="text-xs text-dark-gray">{{ stand.description }}</p>
      <!-- form -->
      <div class="w-full py-4" v-show="stand.id == standSelected">
        <hr class="w-full bg-gray-600" />
        <div class="flex w-full justify-between items-center pt-4">
          <p class="text-gray-600">Enter your pledge</p>
          <input
            type="number"
            v-model="amount"
            class="rounded-full border-2 border-gray-600 w-32 text-dark-cyan"
          />
          <button class="px-6 py-2 bg-dark-cyan rounded-full" @click="submitDataStand">Submit</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    submitDataStand () {
      let stand = {stand:{...this.stand}, amount: this.amount};
      stand.stand.left--;
      this.$emit('submitDataStand', stand)
    }
  },
  props: {
    stand: { type: Object },
    standSelected: { type: Number },
    handleStandSelect: { type: Function },
  },
  data () {
    return {
      amount: this.stand.min_price,
    }
  },
}
</script>

<style>
</style>