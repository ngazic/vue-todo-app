<template>
  <div class="todo-item">
    <h1>{{ text }}</h1>
  </div>
</template>

<script>
export default {
  name: 'todoItem',
  props: {
    text: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
