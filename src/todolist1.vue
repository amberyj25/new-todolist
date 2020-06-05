<template>
  <div>
    <todoInput1 @addEmitTodo="addTodo"></todoInput1>
    <ul>
      <todoItem1
        v-for="(item, index) in todolist"
        :newItem="item"
        @click.native="spliceTodolist(index)"
      ></todoItem1>
    </ul>
  </div>
</template>

<script>
import todoInput1 from "./todoInput1.vue";
import todoItem1 from "./todoItem1.vue";
export default {
  components: {
    todoInput1,
    todoItem1
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
