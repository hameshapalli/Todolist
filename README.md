# Todolist


<!DOCTYPE html>
<html>
<head>
  <title>To Do List</title>
  <style>
    body {
      background: #e3f2fd;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      font-family: Arial;
    }

    .box {
      background: white;
      padding: 20px;
      width: 300px;
      border-radius: 10px;
    }

    input {
      width: 75%;
      padding: 8px;
    }

    button {
      padding: 8px;
      cursor: pointer;
    }

    li {
      margin: 8px 0;
    }
  </style>
</head>

<body>

<div class="box">
  <h2>My To-Do List</h2>
  <input type="text" id="task">
  <button onclick="addTask()">Add</button>

  <ul id="list"></ul>
</div>

<script>
  function addTask() {
    let task = document.getElementById("task").value;

    if (task == "") {
      alert("Enter a task");
    } else {
      let li = document.createElement("li");
      li.innerHTML = task + " <button onclick='removeTask(this)'>X</button>";
      document.getElementById("list").appendChild(li);
      document.getElementById("task").value = "";
    }
  }

  function removeTask(btn) {
    btn.parentElement.remove();
  }
</script>

</body>
</html>
