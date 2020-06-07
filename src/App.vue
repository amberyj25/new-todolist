<template>
  <div>
    <h1>todolist (todoInput component 的兩種寫法)</h1>
    <div class="todolistOne">
      <h2>（一）todolist - todoInput - 用form的寫法</h2>
      <todolist1></todolist1>
    </div>
    <div class="todolistTwo">
      <h2>（二）todolist - todoInput - 沒有用form的寫法</h2>
      <todolist2></todolist2>
    </div>
  </div>
</template>

<script>
import todolist1 from "./todolist1.vue";
import todolist2 from "./todolist2.vue";
export default {
  components: {
    todolist1,
    todolist2
  }
};
</script>

<style scoped>
h2 {
  color: blue;
}
</style>
