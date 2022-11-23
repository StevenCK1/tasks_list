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
    <button v-on:click="saveNewTask">Save new task</button>
    <div>{{ number }}</div>
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
    saveNewTask: function () {
      // counter for the order task was added
      this.number++;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
