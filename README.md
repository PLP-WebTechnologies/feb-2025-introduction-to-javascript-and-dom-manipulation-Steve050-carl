# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨



<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>JavaScript and DOM Manipulation</title>
  <link rel="stylesheet" href="style.css">
  <script src="script.js" defer></script>
</head>
<body>

  <header>
    <h1 id="mainHeading">Welcome to My Web Page!</h1>
  </header>

  <section>
    <p id="introText">This is a simple introduction to JavaScript and DOM manipulation.</p>
    <button id="changeTextBtn">Change Text</button>
    <button id="changeStyleBtn">Change Style</button>
    <button id="addElementBtn">Add Element</button>
    <button id="removeElementBtn">Remove Element</button>
  </section>

  <footer>
    <p>&copy; 2025 JavaScript Learner</p>
  </footer>

</body>
</html>


// Change text content dynamically
document.getElementById("changeTextBtn").addEventListener("click", function () {
  document.getElementById("introText").textContent = "You clicked the button — text changed!";
});

// Modify CSS styles via JavaScript
document.getElementById("changeStyleBtn").addEventListener("click", function () {
  document.body.style.backgroundColor = "#f0f8ff";
  document.getElementById("mainHeading").style.color = "#ff6347";
});

// Add a new element when button is clicked
document.getElementById("addElementBtn").addEventListener("click", function () {
  let newPara = document.createElement("p");
  newPara.textContent = "✨ A new paragraph was added!";
  newPara.id = "newPara";
  document.body.appendChild(newPara);
});

// Remove the new element when button is clicked
document.getElementById("removeElementBtn").addEventListener("click", function () {
  let paraToRemove = document.getElementById("newPara");
  if (paraToRemove) {
    paraToRemove.remove();
  }
});

