<template>
  <div>
    <input
      type="text"
      v-model="todo"
      @keydown.enter="emitTodo"
      placeholder="請輸入文字"
    />
    <button @click.prevent="emitTodo">submit</button>
  </div>
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
      this.$emit("addemitTodo", this.todo);
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
