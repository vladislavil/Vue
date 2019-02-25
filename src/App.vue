<template>
  <div id="app">

    <app-counter></app-counter>
    <app-car></app-car>

  </div>
</template>

<script>

import Car from './car'
import Counter from './counter'

export default {
  components: {
    appCar: Car,
    appCounter: Counter
  }
}
</script>

<style lang="sass">

</style>
