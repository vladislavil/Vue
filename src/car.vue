<template>
  <div class="car">
    <slot name="title"></slot>
    <hr>
    <hr>
    <slot name="text"></slot>
  </div>
</template>

<script>

export default {

}

</script>

<style lang="sass" scoped>
  div
    border: 2px solid #000
    padding-bottom: 10px
    padding-left: 10px
</style>
