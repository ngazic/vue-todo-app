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
        // {id:1,title:'first'},
        // {id:2,title:'second'},
        // {id:3,title:'third'},
        // {id:4,title:'forth'}
      ]
    }
  },
  created() {
    axios.get('https://jsonplaceholder.typicode.com/todos?_limit=10')
    .then(res => this.list = res.data)
    .catch(err => console.log(err));
  }
  }
</script>
