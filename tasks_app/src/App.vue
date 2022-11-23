<template>
  <div id="app">
    <TaskInput @clicked="handleClick" />
    <button v-on:click="toggleView">
      {{ isPriority ? "Sort by order added" : "Sort by priority" }}
    </button>

    <TaskListItems :task-list="taskList" @remove="taskList.splice(index, 1)" />
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
      isPriority: false,
    };
  },
  methods: {
    handleClick(value) {
      // add newTask object from TaskInput component and push to taskList array within data
      this.taskList.push(value);
    },
    toggleView() {
      // reverse boolean for toggle view
      this.isPriority = !this.isPriority;
      //call computed sortTaskList function
      this.sortTaskList;
    },
  },
  computed: {
    // Logic is to manipulate the taskList array to display task in the wanted order
    sortTaskList() {
      let sortedTasks = this.taskList;

      if (this.isPriority) {
        // sort by priorityNumber
        sortedTasks = sortedTasks.sort((a, b) => {
          return a.priorityNumber - b.priorityNumber;
        });
      } else if (!this.isPriority) {
        // sort by order dated (i.e. by id)
        sortedTasks = sortedTasks.sort((a, b) => {
          return a.id - b.id;
        });
      }
      return sortedTasks;
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
