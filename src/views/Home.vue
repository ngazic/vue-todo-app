<template>
  <div class="home">
    <HelloWorld title="this is todo title"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/todo.vue'

export default {
  name: 'home',
  components: {
    HelloWorld
  }
}
</script>
