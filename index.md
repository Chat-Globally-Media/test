

<!DOCTYPE html>
<html lang="en" >

<head>

  <meta charset="UTF-8">
  
<link rel="apple-touch-icon" type="image/png" href="https://cpwebassets.codepen.io/assets/favicon/apple-touch-icon-5ae1a0698dcc2402e9712f7d01ed509a57814f994c660df9f7a952f3060705ee.png" />
<meta name="apple-mobile-web-app-title" content="CodePen">

<link rel="shortcut icon" type="image/x-icon" href="https://cpwebassets.codepen.io/assets/favicon/favicon-aec34940fbc1a6e787974dcd360f2c6b63348d4b1f4e06c77743096d55480f33.ico" />

<link rel="mask-icon" type="image/x-icon" href="https://cpwebassets.codepen.io/assets/favicon/logo-pin-8f3771b1072e3c38bd662872f6b673a722f4b3ca2421637d5596661b4e2132cc.svg" color="#111" />


  <title>CodePen - To-Do App</title>
  <link href='https://fonts.googleapis.com/css?family=Lato:400,700,900' rel='stylesheet' type='text/css'>
<script src="https://use.typekit.net/hoy3lrg.js"></script>
<script>try{Typekit.load({ async: true });}catch(e){}</script>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/meyer-reset/2.0/reset.min.css">

  
  
<style>
@charset "UTF-8";
/* Flat UI Colors */
.alizarin {
  background: #e74c3c !important;
}

.sun-flower {
  background: #f1c40f !important;
}

.emerald {
  background: #2ecc71 !important;
}

/* Font with fallback */
/*--------*/
/* Mixins */
/*--------*/
/* Transition */
/* Border Radius */
/* Box-shadow */
/* User Select */
/* Filter */
/* Appearance */
/* Aspect Ratio */
/* Transform Base */
/* Transform - Scale */
/* Transform - Translate */
/* Transform - Skew */
/* Transform - Origin */
/* Linear Gradient */
/* Calculate REM */
/*---------*/
/* Presets */
/*---------*/
/* body */
body {
  background: #ecf0f1;
  font-family: "proxima-nova", "Lato", "Source Sans Pro", "Raleway", Arial, sans-serif;
  height: 100vh;
  width: 100vw;
}

/* Float: left/right */
.pull-left {
  float: left;
}

.pull-right {
  float: right;
}

/* Flex center */
.flex-center {
  display: -webkit-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
  -webkit-flex-align: center;
  -ms-flex-align: center;
  -webkit-align-items: center;
  align-items: center;
  justify-content: center;
}

/* Flex */
.flex {
  display: -webkit-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
}

/* Outline none */
*, *:focus, *:active {
  outline: none;
}

.clearfix:after {
  content: "";
  display: table;
  clear: both;
}

li.task:nth-child(6n+1)::after {
  background: #e74c3c;
  background: -webkit-linear-gradient(left, #e74c3c, #d62c1a);
  background: linear-gradient(to right, #e74c3c, #d62c1a);
}
li.task:nth-child(6n+1)::before {
  color: #e74c3c;
}

li.task:nth-child(6n+2)::after {
  background: #2ecc71;
  background: -webkit-linear-gradient(left, #2ecc71, #25a25a);
  background: linear-gradient(to right, #2ecc71, #25a25a);
}
li.task:nth-child(6n+2)::before {
  color: #2ecc71;
}

li.task:nth-child(6n+3)::after {
  background: #3498db;
  background: -webkit-linear-gradient(left, #3498db, #217dbb);
  background: linear-gradient(to right, #3498db, #217dbb);
}
li.task:nth-child(6n+3)::before {
  color: #3498db;
}

li.task:nth-child(6n+4)::after {
  background: #f1c40f;
  background: -webkit-linear-gradient(left, #f1c40f, #c29d0b);
  background: linear-gradient(to right, #f1c40f, #c29d0b);
}
li.task:nth-child(6n+4)::before {
  color: #f1c40f;
}

li.task:nth-child(6n+5)::after {
  background: #9b59b6;
  background: -webkit-linear-gradient(left, #9b59b6, #804399);
  background: linear-gradient(to right, #9b59b6, #804399);
}
li.task:nth-child(6n+5)::before {
  color: #9b59b6;
}

li.task:nth-child(6n+6)::after {
  background: #1abc9c;
  background: -webkit-linear-gradient(left, #1abc9c, #148f77);
  background: linear-gradient(to right, #1abc9c, #148f77);
}
li.task:nth-child(6n+6)::before {
  color: #1abc9c;
}

body {
  height: auto;
  width: 100vw;
  background: #ecf0f1;
  font-family: "proxima-nova", "Lato", "Source Sans Pro", "Raleway", Arial, sans-serif;
  overflow-x: hidden;
}

button {
  border: none;
  background: transparent;
}

div#wrapper {
  margin: 10vh auto 0;
  width: 80%;
  max-width: 500px;
  text-align: center;
}
div#wrapper div#input, div#wrapper div#tasks {
  width: 100%;
}

h2 {
  font-size: 36px;
  font-weight: 700;
}

p.sub-title {
  font-size: 16px;
  margin: 10px 0 40px;
}
p.sub-title a {
  border-bottom: 1px solid black;
  color: black;
  padding: 0 1px;
  text-decoration: none;
  -webkit-transition: all 0.3s ease;
  -moz-transition: all 0.3s ease;
  -ms-transition: all 0.3s ease;
  -o-transition: all 0.3s ease;
  transition: all 0.3s ease;
}
p.sub-title a:hover {
  border-color: #27ae60;
  color: #27ae60;
  padding: 0 1px 1px;
}

span#error {
  background: #e74c3c;
  border-radius: 8px;
  color: white;
  display: inline-block;
  margin: 0 auto;
  opacity: 0;
  padding: 6px 16px;
  position: relative;
  top: 0px;
  -webkit-transition: all 0.3s ease;
  -moz-transition: all 0.3s ease;
  -ms-transition: all 0.3s ease;
  -o-transition: all 0.3s ease;
  transition: all 0.3s ease;
}
span#error::after {
  border-left: 8px solid transparent;
  border-right: 8px solid transparent;
  border-top: 8px solid #e74c3c;
  content: "";
  height: 0;
  left: calc(50% - 8px);
  position: absolute;
  top: 27px;
  width: 0;
}
span#error.active {
  opacity: 1;
  top: -12px;
}

div#input {
  border-radius: 8px;
  -webkit-box-shadow: 0px 2px 5px 0px #cfd9db;
  -moz-box-shadow: 0px 2px 5px 0px #cfd9db;
  box-shadow: 0px 2px 5px 0px #cfd9db;
  font-size: 0;
  height: 40px;
  line-height: 40px;
  overflow: hidden;
  position: relative;
}
div#input input {
  background: white;
  border: none;
  font-family: "proxima-nova", "Lato", "Source Sans Pro", "Raleway", Arial, sans-serif;
  height: 100%;
  padding: 0 12px;
  width: calc(100% - 64px);
}
div#input button {
  background: #2ecc71;
  color: white;
  cursor: pointer;
  font-size: 18px;
  height: 101%;
  width: 40px;
}
div#input button:hover {
  background: #2cc26b;
}

div#tasks {
  margin: 20px 0 60px;
  text-align: left;
}
div#tasks ol {
  position: relative;
  counter-reset: list-counter;
}
div#tasks ol li.task {
  background: white;
  border-radius: 8px;
  -webkit-box-shadow: 0px 2px 5px 0px #cfd9db;
  -moz-box-shadow: 0px 2px 5px 0px #cfd9db;
  box-shadow: 0px 2px 5px 0px #cfd9db;
  font-size: 20px;
  height: 60px;
  line-height: 61px;
  margin: 8px 0 0;
  overflow: hidden;
  padding: 0 12px 0 14px;
  position: relative;
}
div#tasks ol li.task::before {
  content: counter(list-counter);
  counter-increment: list-counter;
  float: left;
  font: "proxima-nova", "Lato", "Source Sans Pro", "Raleway", Arial, sans-serif;
  font-weight: 600;
  font-feature-settings: "tnum" on;
  font-variant-numeric: tabular-nums;
  margin: 0 10px 0 5px;
}
div#tasks ol li.task::after {
  bottom: 0;
  content: "";
  height: 3px;
  left: 0;
  position: absolute;
  width: 100%;
}
div#tasks ol li.task:hover {
  -webkit-transition: box-shadow 0.3s ease-in-out;
  -moz-transition: box-shadow 0.3s ease-in-out;
  -ms-transition: box-shadow 0.3s ease-in-out;
  -o-transition: box-shadow 0.3s ease-in-out;
  transition: box-shadow 0.3s ease-in-out;
  -webkit-box-shadow: 0px 2px 5px 0px #a3b6bb;
  -moz-box-shadow: 0px 2px 5px 0px #a3b6bb;
  box-shadow: 0px 2px 5px 0px #a3b6bb;
}
div#tasks ol li.task:hover p {
  width: calc(100% - 135px);
}
div#tasks ol li.task:hover button {
  -webkit-transition: opacity 0.25s ease;
  -moz-transition: opacity 0.25s ease;
  -ms-transition: opacity 0.25s ease;
  -o-transition: opacity 0.25s ease;
  transition: opacity 0.25s ease;
  opacity: 1;
}
div#tasks ol li.task.completed {
  animation-duration: 1s;
  animation-fill-mode: both;
  animation-name: zoomOut;
}
div#tasks ol li.task.completed::after {
  content: "";
  color: white;
  font-family: FontAwesome;
  font-size: 30px;
  height: 100%;
  text-align: center;
}
div#tasks ol li.task:nth-child(n+10):hover p {
  width: calc(100% - 144px);
}
div#tasks ol li.task:nth-child(n+10) p {
  width: calc(100% - 40px);
}
div#tasks ol li.task:nth-child(n+10) input.editable {
  left: 53px;
}
div#tasks ol li.task p {
  display: inline-block;
  text-overflow: ellipsis;
  overflow: hidden;
  -webkit-transition: width 0.2s ease;
  -moz-transition: width 0.2s ease;
  -ms-transition: width 0.2s ease;
  -o-transition: width 0.2s ease;
  transition: width 0.2s ease;
  white-space: nowrap;
  width: calc(100% - 30px);
}
div#tasks ol li.task input.editable {
  border: none;
  display: none;
  font-family: "proxima-nova", "Lato", "Source Sans Pro", "Raleway", Arial, sans-serif;
  font-size: 20px;
  left: 41px;
  position: absolute;
  text-overflow: ellipsis;
  top: 17px;
  width: calc(100% - 130px);
}
div#tasks ol li.task button {
  cursor: pointer;
  font-size: 20px;
  opacity: 0;
  -webkit-transition: opacity 0.25s ease;
  -moz-transition: opacity 0.25s ease;
  -ms-transition: opacity 0.25s ease;
  -o-transition: opacity 0.25s ease;
  transition: opacity 0.25s ease;
}
div#tasks ol li.task button.complete {
  color: #2ecc71;
}
div#tasks ol li.task button.edit, div#tasks ol li.task button.save {
  color: #3498db;
}
div#tasks ol li.task button.delete, div#tasks ol li.task button.cancel {
  color: #e74c3c;
}
div#tasks ol li.task button.save, div#tasks ol li.task button.cancel {
  display: none;
  opacity: 1 !important;
}
div#tasks ol li.task button i {
  margin-left: 4px;
}
div#tasks ol li.task div.button-wrap {
  float: right;
  font-size: 0;
  line-height: 72px;
}

@keyframes zoomOut {
  from {
    opacity: 1;
  }
  50% {
    opacity: 0;
    transform: scale3d(1.15, 1.15, 1.15);
  }
}
</style>

  <script>
  window.console = window.console || function(t) {};
</script>

  
  
  <script>
  if (document.location.search.match(/type=embed/gi)) {
    window.parent.postMessage("resize", "*");
  }
</script>


</head>

<body translate="no" >
  <div id="wrapper">
	<h2>To-Do</h2>
	<p class="sub-title">A pen by <a href="https://codepen.io/emilcarlsson/">Emil Carlsson</a></p>
	<span id="error">Lorem ipsum</span>
	<div id="input">
		<input type="text">
		<button id="add-task" title="Add new task"><i class="fa fa-plus fa-fw" aria-hidden="true"></i></button>
	</div>
	<div id="tasks">
		<ol>
		</ol>
	</div>
</div>
    <script src="https://cpwebassets.codepen.io/assets/common/stopExecutionOnTimeout-1b93190375e9ccc259df3a57c1abc0e64599724ae30d7ea4c6877eb615f89387.js"></script>

  <script src='https://cdnjs.cloudflare.com/ajax/libs/jquery/3.2.1/jquery.min.js'></script>
<script src='https://use.fontawesome.com/15af25ac7b.js'></script>
      <script id="rendered-js" >
$(document).ready(function () {
  // Focus input on load
  $("#input input").focus();

  // Example tasks
  if (localStorage.getItem("first") === null) {
    var exampleTasks = [
    "Finish History paper",
    "Go for a walk",
    "Take out the trash",
    "Feed cat",
    "Read A Clash of Kings",
    "Shop for groceries"];

    localStorage.setItem("tasks", JSON.stringify(exampleTasks));
    localStorage.setItem("first", "0");
  }

  // Loading stored tasks
  var storedTasks = JSON.parse(localStorage.getItem("tasks"));
  for (i = 0; i < storedTasks.length; i++) {if (window.CP.shouldStopExecution(0)) break;
    $("ol").append(createTask(storedTasks[i]));
  }window.CP.exitedLoop(0);
  $("li.task").show();
  storeData();
});

// Create task
function createTask(taskText) {
  return $('<li class="task">' +
  '<p title="' + taskText + '">' + taskText + '</p>' +
  '<input type="text" class="editable" value="' + taskText + '">' +
  '<div class="button-wrap">' +
  '<button title="Complete" class="complete"><i class="fa fa-check" aria-hidden="true"></i></button>' +
  '<button title="Edit" class="edit"><i class="fa fa-pencil" aria-hidden="true"></i></button>' +
  '<button title="Delete" class="delete"><i class="fa fa-trash" aria-hidden="true"></i></button>' +
  '<button title="Save" class="save"><i class="fa fa-floppy-o" aria-hidden="true"></i></button>' +
  '<button title="Cancel" class="cancel"><i class="fa fa-times" aria-hidden="true"></i></button>' +
  '</div></li>').hide();
};

// Add new task
$("#add-task").click(function () {
  if (!$("#input input").val()) {
    error("The input field is empty.");
  } else {
    $("#error").removeClass("active");
    var newTask = createTask($("#input input").val());
    $("#tasks ol").append(newTask);
    newTask.slideDown();
    $("#input input").val('');
    $("#input input").focus();
    storeData();
  }
});

// Complete a task
$("#tasks ol").on("click", ".complete", function () {
  $(this).parents("li.task").addClass("completed");
  $(this).parents("li.task").animate({
    opacity: 0 },
  300, 'linear', function () {
    $(this).remove();
    storeData();
  });
});

// Delete a task
$("#tasks ol").on("click", ".delete", function () {
  $(this).parents("li.task").animate({
    opacity: 0,
    left: '-200px' },
  300, 'linear', function () {
    $(this).remove();
    storeData();
  });
});

// Edit a task
$("#tasks ol").on("click", ".edit", function () {
  $(this).closest("li.task").find("p").css("display", "none");
  $(this).closest("li.task").find(".editable").css("display", "block");
  $(this).closest("li.task").find(".editable").focus().val('').val($(this).closest("li.task").find("p").html());
  $(this).parent().find("button").css("display", "none");
  $(this).parent().find(".save, .cancel").css("display", "inline-block");
});

// Save edited task
$("#tasks ol").on("click", ".save", function () {
  $(this).closest("li.task").find("p").html($(this).closest("li.task").find(".editable").val()); // Setting the HTML of <p> to the input value
  $(this).closest("li.task").find(".editable").css("display", "none");
  $(this).closest("li.task").find("p").css("display", "inline-block");
  $(this).parent().find("button").css("display", "inline-block");
  $(this).parent().find(".save, .cancel").css("display", "none");
  storeData();
});

// Cancel edited task
$("#tasks ol").on("click", ".cancel", function () {
  $(this).closest("li.task").find(".editable").css("display", "none");
  $(this).closest("li.task").find("p").css("display", "inline-block");
  $(this).parent().find("button").css("display", "inline-block");
  $(this).parent().find(".save, .cancel").css("display", "none");
});

// Store data in localStorage
function storeData() {
  // Clearing existing storage
  localStorage.removeItem("tasks");

  // Store tasks in array
  var tasksArray = [];
  $("li.task p").each(function () {tasksArray.push($(this).html());});

  // Store the array in localStorage
  localStorage.setItem("tasks", JSON.stringify(tasksArray));
};

// Error
function error(message) {
  $("#error").html(message);
  $("#error").addClass("active");
};
//# sourceURL=pen.js
    </script>

  

</body>

</html>
 
