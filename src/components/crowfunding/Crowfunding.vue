<template>
  <div class="crowfunding-container flex flex-col justify-center space-y-6">
    <Header/>
    <Backers/>
    <About/>
    <Overlay/>
  </div>
</template>

<script>
import Backers from "./backers/Backers.vue";
import Header from "./header/Header.vue";
import About from "./about/About.vue";
import Overlay from "./overlay/Overlay.vue";
export default {
    name: "Crowfunding",
    components: { Header, Backers, About, Overlay }
}
</script>

<style scoped>

.crowfunding-container {
  width: 728px;
}
</style>