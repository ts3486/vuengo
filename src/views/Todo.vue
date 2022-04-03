<template>
  <div id="todoPage">
    <todo-input />
    <todo-column :todos="todos" />
    {{ print }}
  </div>
</template>

<script>
import TodoColumn from "../components/TodoColumn.vue";
import TodoInput from "../components/TodoInput.vue";

export default {
  data() {
    return {
      todos: this.$store.state.todos,
    };
  },
  components: {
    TodoColumn,
    TodoInput,
  },
  computed: {
    print() {
      return console.log(this.$store.state.todos);
    },
  },
};
</script>
