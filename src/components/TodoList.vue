<template>
  <div>
    <input type="text" class="todo-input" placeholder="What you gotta do?" 
    v-model="newTodo" @keyup.enter="addTodo" />
    <div v-for="todo in todos" :key="todo.id" class="todo-item">
        {{ todo.title }}
    </div>
  </div>
</template>

<script>
export default {
  name: "todo-list",
  data() {
    return {
      newTodo: "",
      todos: [
        {
          id: 1,
          title: "Finish Vue Screen",
          completed: false
        },
        {
          id: 2,
          title: "Beat this level",
          completed: false
        },
        {
          id: 3,
          title: "Get a job",
          completed: false
        }
      ]
    };
  },
  methods: {
      addTodo() {
          alert('adding todo')
      }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.todo-input {
  width: 100%;
  padding: 10px 18px;
  font-size: 18px;
  margin-bottom: 16px;
}
</style>
