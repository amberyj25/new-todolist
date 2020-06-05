<template>
  <div>
    <todoInput2 @addemitTodo="addTodo"></todoInput2>
    <ul>
      <todoItem2
        v-for="(item, index) in todolist"
        :newTodo="item"
        @click.native="spliceTodolist(index)"
      ></todoItem2>
    </ul>
  </div>
</template>

<script>
import todoInput2 from "./todoInput2.vue";
import todoItem2 from "./todoItem2.vue";
export default {
  components: {
    todoInput2,
    todoItem2
  },
  data() {
    return {
      todolist: []
    };
  },
  methods: {
    addTodo(todo) {
      this.todolist.push(todo);
    },
    spliceTodolist(index) {
      this.todolist.splice(index, 1);
    }
  }
};
</script>
