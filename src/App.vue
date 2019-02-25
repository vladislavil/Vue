<template>
  <!--nameCanged - считываем изменения переменной carName из дочернего компонента-->
  <div id="app">
    <h1>Parent: {{ carName }}</h1>

    <app-counter
    ></app-counter>

    <app-car
      :carYear="carYear"
      :carName="carName"
      @nameChanged = "carName = $event"
      :changeFunc = "changeNameToAudi"
    ></app-car>
  </div>
</template>

<script>

import Car from './car'
import Counter from './counter'

export default {
  data () {
    return {
      carName: 'Ford',
      carYear: 2015,
    }
  },
  components: {
    appCar: Car,
    appCounter: Counter
  },
  methods: {
    changeNameToAudi: function () {
      return this.carName = "Audi"
    },
  }
}
</script>

<style lang="sass">
  h1
    color: red
</style>
