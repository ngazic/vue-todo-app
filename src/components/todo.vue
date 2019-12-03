<template>
<div class="todo">
    <h1>title is: {{ title }}</h1>
    <div class="todo__wrapper">
      <input type="text" class="todo__input" v-model="text"  placeholder="Add todo....">
      <button class="todo__button" @click="addNewTodo">Add</button>
    </div>
    <ul class="todo__list">
    <todoItem v-for="todo in todos" v-bind:key="todo.id" :todo="todo" ></todoItem>  
  </ul>
</div>
</template>

<script>
// @ is an alias to /src
import todoItem from "@/components/atoms/todo-item.vue";

export default {
  name: "todo",
  components: {
    todoItem
  },
  methods: {
    addNewTodo: function () {
      // alert(this.title);
      var ID = this.todos.length;
      console.log("object is ");
      var ob = {id: ID, title: this.text}
      console.log(ob);
      this.todos.push(ob);
      this.text = '';
    }
  },
  props: {
    todos: Object,
    title: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.todo {
  background-color: rgba(100, 100, 100, 0.1);
  
  h1 {
    background: rgba(blue, 0.1);
  }

  &__wrapper {
    display: flex;
    align-items: center;
    flex-flow: row;
    justify-content: center;
  }

  &__input {
    border-radius: 10px;
    border: 2px solid black;
    display: inline-block;
  }

  &__button {
    height:100%;
    border: 2px solid black;
    background:rgba(blue, 0.1);
    margin: 0 10px
  }
}
</style>
