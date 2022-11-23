<template>
  <div class="taskInput">
    <h2>Create a new task</h2>

    <label for="textInput">Task description:</label>
    <input v-model="message" id="taskInputText" />
    <label for="priorityNumber"
      >Set the priority of the task (1 is most urgent, 10 is least
      urgent):</label
    >
    <select v-model.number="selected" id="priorityNumber">
      <option disabled value="">Please Select</option>
      <option v-for="option in options" :key="option">{{ option }}</option>
    </select>
    <button v-on:click="handleClick">Save new task</button>
  </div>
</template>

<script>
export default {
  name: "TaskInput",
  data() {
    return {
      message: "",
      selected: "",
      options: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10],
      number: 0,
    };
  },
  methods: {
    handleClick: function () {
      // counter for the order that the  new task was added
      this.number++;

      // Add new task object to taskList array
      const newTask = {
        taskDescription: this.message,
        priorityNumber: this.selected,
        id: this.number,
      };

      // emit taskList to parent
      this.$emit("clicked", newTask);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
