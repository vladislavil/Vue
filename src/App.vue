<template>
  <div id="app">
    <h1 v-colored v-if="visible"> {{ title }} </h1>
    <button @click="visible = !visible">Toggle</button>
    <button @click="title = 'new title'">Toggle</button>
  </div>
</template>

<script>

export default {

  data() {
   return  {
     visible: true,
     title: "Hello i am Vue"
   }
  }
}
</script>

<style lang="sass">

</style>
