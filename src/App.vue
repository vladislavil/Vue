<template>
  <div id="app">
    <h1>Parent: {{ carName }}</h1>
    <app-car :carName="carName" :carYear="carYear"></app-car>
  </div>
</template>

<script>

import Car from './car'

export default {
  data () {
    return {
      carName: 'Ford from parent',
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
