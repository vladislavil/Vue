<template>
  <div id="app">

    <app-car>

      <h1 slot="title"> {{carName}} </h1>
      <p slot="text">Lorem ipsum dolor sit amet.</p>

    </app-car>

  </div>
</template>

<script>

import Car from './car'

export default {

  data() {
   return  {
     carName: "Ford"
   }
  },
  components: {
    appCar: Car
  }
}
</script>

<style lang="sass">

</style>
