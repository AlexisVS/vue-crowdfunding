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
        <svg
          @click="$emit('closeOverlay', true)"
          class="absolute top-5 right-5 fill-current text-black cursor-pointer"
          fill="black"
          width="15"
          height="15"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M11.314 0l2.828 2.828L9.9 7.071l4.243 4.243-2.828 2.828L7.07 9.9l-4.243 4.243L0 11.314 4.242 7.07 0 2.828 2.828 0l4.243 4.242L11.314 0z"
            fill="currentColor"
          />
        </svg>
        <h2 class="font-bold mt-2 text-xl text-black">Back this project</h2>
        <p
          class="text-dark-gray text-xs my-5"
        >Wan to support us in bringing Mastercraft Bamboo Monitor Riser out in the world?</p>
        <!-- Stand with no pledge -->
        <div class="w-full h-full flex flex-col items-center space-y-4">
          <div class="border-2 border-gray-300 rounded-lg flex py-6" @click="standSelect(0)">
            <div class="w-16 flex justify-center">
              <input
                type="radio"
                class="bg-gray-100 border-0 mt-0.5 ring-2 ring-dark-cyan caret-dark-cyan text-dark-cyan outline-none"
                name="inputRadioOverlayStand"
                :value="0"
                :checked="standSelected == null || standSelected == 0"
              />
            </div>
            <div class="w-full pr-4">
              <div class="w-full mb-6 flex items-center justify-between">
                <h3 class="text-dark-cyan font-">Pledge with no reward</h3>
                <div class="flex items-center">
                  <span class="font-bold text-black">101</span>
                  <span class="text-base text-dark-gray ml-2.5">left</span>
                </div>
              </div>
              <p
                class="text-xs text-dark-gray"
              >Choose to support us whithout a reward if you simply believe in our project. As a backer you will be signed up to receive product updates via email.</p>
            </div>
          </div>
          <Stand
            v-for="stand in data"
            :key="'stand' + stand.id"
            :stand="stand"
            :standSelected="standSelected"
            :handleStandSelect="standSelect"
            @submitDataStand="submitDataStand"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Stand from "./Stand.vue";
export default {
  name: "Overlay",
  components: { Stand },
  data () {
    return {
      // le input selection par l'id
      // standSelected: null,
    }
  },
  methods: {
    submitDataStand (data) {
      this.$emit('submitDataStand', data);
    }
  },
  props: {
    data: {
      type: Object,
    },
    standSelected: { type: Number },
    standSelect: { type: Function },
  }
}
</script>

<style scoped>
.overlay {
  margin: 0 !important;
}
.w-overlay {
  width: 500px;
}
</style>