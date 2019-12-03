<template>
  <li class="todo-item">
    <h1>{{  todo.id  }}.{{ todo.title }}</h1>
  <button class="todo-item__button">X</button>
  </li>
</template>

<script>
export default {
  name: 'todoItem',
  props: {
    todo: Object
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.todo-item {
  list-style: none;
  display: flex;
  flex-flow: row wrap;
  align-items: center;
  justify-content: center;
  
  h1 {
    display:inline-block;
    flex-grow: 1;
  }

  &__button {
    border-radius: 50%;
    box-shadow: 0 0 10px rgba(8, 8, 8,0.8);
  }
}
</style>
