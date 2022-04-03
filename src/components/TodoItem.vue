<template>
  <v-item v-slot="{ active, toggle }">
    <v-card :color="active ? 'primary' : ''" class="d-flex align-center" dark height="200" @click="toggle">
      <v-scroll-y-transition>
        <div v-if="active" class="text-h2 flex-grow-1 text-center">{{ todo }}</div>
      </v-scroll-y-transition>
    </v-card>
  </v-item>
</template>

<script>
export default {
  name: "TodoItem",
  props: ["todo"],
  computed: {
    print() {
      return console.log(this.todo.id);
    },
  },
};
</script>
