<template>
  <b-container>
    <h1>Risk of Rain 2 Damage Calculator</h1>
    <h2>Last update: <a href="https://steamcommunity.com/games/632360/announcements/detail/4642591179202236270"> Build ID #4892828</a> </h2>
    <br>
    <br>
    <b-row>
      <b-col>
        <b-btn
          variant="success"
          href="survivors/"
        >
          <img :src="getImage()">
          Get started
        </b-btn>
      </b-col>
      <b-col>
        <b-btn
          variant="primary"
          href="learnMore/"
        >
          Learn More
        </b-btn>
      </b-col>
      <b-col>
        <b-btn
          variant="dark"
          href="https://github.com/Darkoyd/RiskOfRainDamageCalculator"
        >
          <font-awesome-icon size="lg" :icon="['fab', 'github']" />
          Source Code
        </b-btn>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  name: 'Index',
  data () {
  },
  methods: {
    getImage () {
      return require('assets/Small_Chest.png')
    }
  }
}
</script>

<style>

</style>
