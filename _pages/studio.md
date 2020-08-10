---
layout: single
permalink: /studio/
title: Studio
classes: wide
header:
  image: /assets/images/stairs.jpg
  image_description: "A description of the image"
---

<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
}

.header {
  text-align: center;
  padding: 32px;
}

.row {
  display: -ms-flexbox; /* IE 10 */
  display: flex;
  -ms-flex-wrap: wrap; /* IE 10 */
  flex-wrap: wrap;
  padding: 0 4px;
}

/* Create two equal columns that sits next to each other */
.column {
  -ms-flex: 50%; /* IE 10 */
  flex: 50%;
  padding: 0 4px;
}

.column img {
  margin-top: 8px;
  vertical-align: middle;
}

/* Style the buttons */
.btn {
  border: none;
  outline: none;
  padding: 10px 16px;
  background-color: #f1f1f1;
  cursor: pointer;
  font-size: 18px;
}

.btn:hover {
  background-color: #ddd;
}

.btn.active {
  background-color: #666;
  color: white;
}
</style>
</head>
<body>

<!-- Header -->
<div class="header" id="myHeader">
  <button class="btn" onclick="one()">1</button>
  <button class="btn active" onclick="two()">2</button>
  <button class="btn" onclick="four()">4</button>
</div>

<!-- Photo Grid -->
<div class="row">
 	<div class="column">
	    <img src="/assets/images/flower1.jpg" style="width:100%">
	    <img src="/assets/images/glass1.jpg" style="width:100%">
	    <img src="/assets/images/street2.jpg" style="width:100%">
	    <img src="/assets/images/dewyleaf.jpg" style="width:100%">
	    <img src="/assets/images/can1.jpg" style="width:100%">
	    <img src="/assets/images/glass3.jpg" style="width:100%">
  	</div>
	<div class="column">
	    <img src="/assets/images/chicago1.jpg" style="width:100%">
	    <img src="/assets/images/brick1.jpg" style="width:100%">
	    <img src="/assets/images/co1.jpg" style="width:100%">
	    <img src="/assets/images/london2.jpg" style="width:100%">
	    <img src="/assets/images/chicago2.jpg" style="width:100%">
	    <img src="/assets/images/co2.jpg" style="width:100%">    
  	</div>
  	<div class="column">
		<img src="/assets/images/co3.jpg" style="width:100%">
	    <img src="/assets/images/street1.jpg" style="width:100%">
	    <img src="/assets/images/ice.jpg" style="width:100%">
	    <img src="/assets/images/street3.jpg" style="width:100%">
	    <img src="/assets/images/lights.jpg" style="width:100%">
	    <img src="/assets/images/time.jpg" style="width:100%">
  	</div>
	<div class="column">
  	 	<img src="/assets/images/brick2.jpg" style="width:100%">
  	 	<img src="/assets/images/london3.jpg" style="width:100%">
	    <img src="/assets/images/london1.jpg" style="width:100%">
	    <img src="/assets/images/flower2.jpg" style="width:100%">
	    <img src="/assets/images/glass2.jpg" style="width:100%">
	    <img src="/assets/images/can2.jpg" style="width:100%">
	</div>
</div>

<script>
// Get the elements with class="column"
var elements = document.getElementsByClassName("column");

// Declare a loop variable
var i;

// Full-width images
function one() {
    for (i = 0; i < elements.length; i++) {
    elements[i].style.msFlex = "100%";  // IE10
    elements[i].style.flex = "100%";
  }
}

// Two images side by side
function two() {
  for (i = 0; i < elements.length; i++) {
    elements[i].style.msFlex = "50%";  // IE10
    elements[i].style.flex = "50%";
  }
}

// Four images side by side
function four() {
  for (i = 0; i < elements.length; i++) {
    elements[i].style.msFlex = "25%";  // IE10
    elements[i].style.flex = "25%";
  }
}

// Add active class to the current button (highlight it)
var header = document.getElementById("myHeader");
var btns = header.getElementsByClassName("btn");
for (var i = 0; i < btns.length; i++) {
  btns[i].addEventListener("click", function() {
    var current = document.getElementsByClassName("active");
    current[0].className = current[0].className.replace(" active", "");
    this.className += " active";
  });
}
</script>

</body>
</html>