<template>
  <div id="app">
    <TaskInput @clicked="handleClick" />
    <TaskListItems />
    <div>{{ taskList }}</div>
  </div>
</template>

<script>
import TaskInput from "./components/TaskInput.vue";
import TaskListItems from "./components/TaskListItems.vue";

export default {
  name: "App",
  components: {
    TaskInput,
    TaskListItems,
  },
  data() {
    return {
      taskList: [],
    };
  },
  methods: {
    handleClick(value) {
      this.taskList.push(value);
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
