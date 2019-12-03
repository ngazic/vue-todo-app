<template>
  <div class="home">
    <todo v-bind:todos="list" title="this is todo title"/>
  </div>
</template>

<script>
// @ is an alias to /src
import todo from '@/components/todo.vue'

export default {
  name: 'home',
  components: {
    todo
  },
  data() {
    return {
      list: [
        {id:0,title:'first'},
        {id:1,title:'second'},
        {id:2,title:'third'},
        {id:3,title:'forth'}
      ]
    }
  }
}
</script>
