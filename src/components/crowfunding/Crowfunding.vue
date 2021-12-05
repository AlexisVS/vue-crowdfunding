<template>
  <div class="crowfunding-container flex flex-col justify-center space-y-6">
    <Header />
    <Backers :data="{ ...crowfunding.statistics }" />
    <About :data="{ ...crowfunding.stands }" />
    <!-- <Overlay :data="{ ...crowfunding.stands }" /> -->
  </div>
</template>

<script>
import Backers from "./backers/Backers.vue";
import Header from "./header/Header.vue";
import About from "./about/About.vue";
// import Overlay from "./overlay/Overlay.vue";
export default {
  name: "Crowfunding",
  components: { Header, Backers, About
  // ,Overlay 
  },
  data () {
    return {
      crowfunding: {
        statistics: {
          backed: {
            current: 89914,
            total: 100000,
          },
          backers: 5007,
          days_left: 56,
        },
        stands: [
          {
            name: 'Bamboo Stand',
            description: "You get an ergonomic stand made of natural bamboo. You've helped us launch our promotional campaign, and you'il be added to a special Backer member list.",
            left: 101,
            min_price: 25,
          },
          {
            name: 'Black Edition Stand',
            description: "You get a Black Special Edition computer stand and a personnal thank you. You'il be added to our Backed member list. Shipping is included.",
            left: 64,
            min_price: 75,
          },
          {
            name: "Mahogany Special Edition",
            description: "You get two Special Edition Mahogany stands, a Backer T-Shirt, and a personal thank you. You'il be added to our Backer member list. Shipping is incuded.",
            left: 1,
            min_price: 200,
          },
        ]
      },
    }
  }
}
</script>

<style scoped>
.crowfunding-container {
  width: 728px;
}
</style>