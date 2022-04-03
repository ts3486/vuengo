<template>
  <v-item-group>
    <v-container>
      <v-row>
        <v-col v-for="todo in this.todos" :key="todo.id" cols="12" md="4">
          <todo-item :todo="todo" />
        </v-col>
      </v-row>
    </v-container>
  </v-item-group>
</template>

<script>
import TodoItem from "../components/TodoItem";

export default {
  name: "TodoColumn",
  components: { TodoItem },
  props: ["todos"],
};
</script>
