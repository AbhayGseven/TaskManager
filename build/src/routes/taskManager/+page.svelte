<script>
    import { Button } from 'flowbite-svelte';
</script>



  <div class="container">
    <h1>Task Manager</h1>
    <ul class="task-list">
        <li class="task-item">
          <input type="checkbox" class="task-checkbox">
          <div class="task-title">Task 1</div>
          <div class="task-date">May 31, 2023</div>
          <div class="task-status ml-4">Pending</div>
          <div class="task-actions">
            <Button class="mr-4 ml-4">Edit</Button>
            <Button>Delete</Button>
          </div>
        </li>
        <li class="task-item">
          <input type="checkbox" class="task-checkbox">
          <div class="task-title">Task 2</div>
          <div class="task-date">May 31, 2023</div>
          <div class="task-status ml-4">Done</div>
          <div class="task-actions">
            <Button class="mr-4 ml-4">Edit</Button>
            <Button>Delete</Button>
          </div>
        </li>
        <!-- Add more tasks as needed -->
      </ul>
      <h1>Add New Task</h1>
      <form class="add-task-form">
        <input type="text" placeholder="Enter task heading" class="task-input">
        <textarea placeholder="Enter task description" class="task-input"></textarea>
        <input type="date" class="task-date">
        <select class="task-priority">
          <option value="high">High Priority (Red)</option>
          <option value="moderate">Moderate Priority (Yellow)</option>
          <option value="low">Low Priority (Green)</option>
        </select>
        <Button class="w-96 m-auto">Add Task</Button>
      </form>
      </div>


<style>
 
h1{
    font-size: 20px;
    font-weight: bold;
    text-decoration: underline;
}
    .container {
    
      margin: 0 auto;
      padding: 20px;
    }

    .task-list {
      list-style-type: none;
      padding: 0;
    }

    .task-item {
      display: flex;
      align-items: center;
      padding: 10px;
      border-bottom: 1px solid #ddd;
    }

    .task-item:last-child {
      border-bottom: none;
    }

    .task-checkbox {
      margin-right: 10px;
    }

    .task-title {
      flex-grow: 1;
      font-size: 18px;
      font-weight: bold;
    }

    .task-date {
      font-size: 14px;
      color: #666;
    }

    .task-actions {
      display: flex;
    }



    .add-task-form {
      display: grid;
      margin-top: 20px;
      gap: 30px;
    }

    .add-task-form input[type="text"] {
      flex-grow: 1;
      padding: 5px;
    }


  </style>
