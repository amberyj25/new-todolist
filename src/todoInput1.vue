<template>
  <form @submit.prevent="emitTodo">
    <input type="text" v-model="todo" placeholder="請輸入文字" />
    <button type="submit">submit</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      todo: ""
    };
  },
  methods: {
    emitTodo() {
      this.$emit("addEmitTodo", this.todo);
      this.todo = "";
    }
  }
};
</script>
<style scoped>
input {
  margin-left: 85px;
}
</style>
