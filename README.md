# tasks_list

Instructions:
Your task is to create a web app that displays a list of tasks, each task has a priority indicating how
urgent the task is (1 is most urgent, 10 is least urgent). You must use vue.js to create the app.

Expected Behaviours:

### The ability to add a new task, with a priority of between 1-10.

1. Input field for new task
2. Dropdown from 1-10 for priority
3. Add counter function for number of save clicks for id generation?
4. Save button to add to an array of object {text, priorityNumber, id}

_Resouce used:_

- [Form Input Binding](https://v2.vuejs.org/v2/guide/forms.html)
- [Event Handling](https://v2.vuejs.org/v2/guide/events.html)
- [Add item to array](https://codingbeautydev.com/blog/vue-add-item-to-array/)

### The ability to view a list of all the tasks

1. Component to have text, priority number (generate each line with id)
2. list components to show different tasks

### The ability to order the tasks by priority or the order they were added to the list

button to order priority

1. check the value number of the key priorityNumber
2. 1 to show on top and 10 at bottom

button to order by time added

1. check the id value

### The ability to delete a task

1. Button next to each task
2. Delete based on ID

### (Optional) The ability to filter to tasks below a certain priority (e.g. display only tasks with a priority

below 3)
