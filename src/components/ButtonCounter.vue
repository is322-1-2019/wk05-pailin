<template>
  <div class="container">
    <button v-on:click="count++">You clicked me {{ count }} times.</button>
    <button v-on:click="countByTwo">You clicked me {{ countt }}  times.</button>
  </div>
</template>

<script>
export default {
  name: 'ButtonCounter',
  data: function() {
    return {
      count: 0,
      countt: 0,
    }
  },
  methods: {
      countByTwo: function(){
          this.countt--;
      }
  }
}
</script>
<style scoped>
</style>