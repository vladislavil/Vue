<template>
  <div id="app">
    <h1>Parent: {{ carName }}</h1>
    <app-car :carYear="carYear"></app-car>
  </div>
</template>

<script>

import Car from './car'

export default {
  data () {
    return {
      carName: 'Ford',
      carYear: 2015
    }
  },
  components: {
    appCar: Car,
  }
}
</script>

<style lang="sass">
  h1
    color: red
</style>
