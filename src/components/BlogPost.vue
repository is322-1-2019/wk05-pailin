<template>
  <div class="container-fluid">
    <h3>{{ title}} id = {{ size }}</h3>
  </div>
</template>

<script>
export default {
  name: 'BlogPost',
  props: [
      'title',
      'size'
    ]
}
</script>
<style scoped>
</style>