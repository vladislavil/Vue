<template>
  <div class="car">
    <h3> Car Name: {{ carName }} \ {{ reverseName }}</h3>
    <p> Car Year: {{ carYear}}</p>
    <button @click="changeName">Change Name</button>
    <button @click="changeFunc()">Change from Parent</button>
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
    carYear: Number,
    changeFunc: Function
  },
  computed: {
    reverseName() {
      return this.carName.split('').reverse().join('');
    }
  },
  methods: {
    changeName: function () {
      this.carName = "Mazda"
      this.$emit('nameChanged', this.carName)// уведомляем родителя, о том, чо carName - был изменен внутри дочернего компонента
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
