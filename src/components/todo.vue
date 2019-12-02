<template>
  <ul class="todo">
    <h1>{{ title }}</h1>
    <div class="todo__wrapper">
      <input type="text" class="todo__input">
      <button class="todo__button" @click="clear">Add</button>
    </div>
    <todoItem text="this is todo item"></todoItem>  
  </ul>
</template>

<script>
// @ is an alias to /src
import todoItem from "@/components/atoms/todo-item.vue";

export default {
  name: "HelloWorld",
  props: {
    title: String
  },
  components: {
    todoItem
  },
  methods: {
    clear: function () {
      // alert(this.title);
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.todo {
  background-color: rgba(100, 100, 100, 0.1);
  
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
