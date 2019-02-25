<template>
  <div class="car">
    <h3> Car Name: {{ carName }} \ {{ reverseName }}</h3>
    <p> Car Year: {{ carYear}}</p>
  </div>
</template>

<script>

export default {
  //props: ['carName', 'carYear'],
  // props: {
  //   carName: String,
  //   carYear: Number
  // },
  props: {
    carName: {
      type: String,
      default: "default CarName"
    },
    carYear: Number
  },
  computed: {
    reverseName() {
      return this.carName.split('').reverse().join('');
    }
  }
}

</script>

<style lang="sass">

  .car
    border: 1px solid black
  h3
    margin-bottom: 5px

</style>
