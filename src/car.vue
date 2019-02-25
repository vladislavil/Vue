<template>
  <div class="car">
    <h3> Car Name: {{ carName }}</h3>
    <p> Car Year: {{ carYear}}</p>
  </div>
</template>

<script>

export default {
  props: ['carName', 'carYear']
}

</script>

<style lang="sass">

  .car
    border: 1px solid black
  h3
    margin-bottom: 5px

</style>
