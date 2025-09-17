# 🎬 Assignment: Bringing Web Pages to Life with CSS & JavaScript

In this assignment, you’ll create a visually dynamic and interactive experience by combining the beauty of **CSS3 animations** with the logic and power of **JavaScript functions**. By the end, you’ll have a mini interactive experience that not only looks good—but *feels* responsive and alive!

---

## 🎨✨ Part 1: CSS3 Transitions and Animations for Dynamic Styling Effects

Start by enhancing elements on your page using **CSS transitions** and **keyframe animations**. You can animate things like:

* Button hover effects
* Smooth fades, slides, or transforms
* Continuous or triggered animations using `@keyframes`

**Goal:** Create a page that visually responds to user interaction and/or time-based triggers using only CSS.

---

## 📚✨ Part 2: JavaScript Functions — Scope, Parameters & Return Values

Now it’s time to dive deeper into how **functions** actually work. In this section:

* Write several custom functions that take in **parameters** and return **useful values**
* Demonstrate understanding of **local vs global scope**
* Show how functions can be reused to control animation, trigger DOM changes, or calculate values

**Goal:** Show functional thinking by building small, reusable pieces of logic that clearly use parameters, return values, and demonstrate scope awareness.

---

## 🎨🎬 Part 3: Combining CSS Animations with JavaScript

Here’s the real magic—combine the two worlds!

Use JavaScript to **trigger** CSS animations dynamically. Think along the lines of:

* A button that animates a box when clicked
* A card flip animation on hover or click
* A loading animation that starts/stops based on user input
* A popup/modal that slides in and fades out based on events

**Goal:** Use JavaScript to **add/remove classes** or modify styles dynamically to trigger CSS animations. Bonus if you make it reusable with functions!

---

## Deliverables

Submit a project folder that includes:

* `index.html` — Your structured content
* `styles.css` — All your transitions and keyframe animations
* `script.js` — Your functional logic demonstrating scope, parameters, return values, and animation triggers

Each part of the assignment should be clearly labeled and commented to show your understanding.

---

## Outcome

You’ll be evaluated on:

* Use of CSS transitions and animations to enhance UI
* Quality and clarity of JavaScript functions (with parameters and return values)
* Effective integration of CSS and JS for interactive effects
* Code readability, modularity, and documentation
* Creativity and user experience

Html File
// Function with parameters and return value
function calculateArea(length, width) {
  return length * width;
}

// Trigger CSS animation with JS
const animateBtn = document.getElementById("animateBtn");
const box = document.getElementById("box");

animateBtn.addEventListener("click", function() {
  // Restart animation
  box.style.animation = "none";
  void box.offsetWidth; // trigger reflow
  box.style.animation = "moveBox 2s ease-in-out";
});

// Handle form submission to calculate area
document.getElementById("areaForm").addEventListener("submit", function(e) {
  e.preventDefault();

  let length = parseFloat(document.getElementById("length").value);
  let width = parseFloat(document.getElementById("width").value);

  if (isNaN(length) || isNaN(width)) {
    document.getElementById("result").textContent = "Please enter valid numbers.";
    return;
  }

  let area = calculateArea(length, width);
  document.getElementById("result").textContent = `The area is ${area}.`;
});

Styles.css
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background: #f4f4f9;
  color: #333;
}

header, footer {
  text-align: center;
  background: #3498db;
  color: #fff;
  padding: 1rem;
}

main {
  padding: 2rem;
  text-align: center;
}

button {
  background: #3498db;
  color: white;
  border: none;
  padding: 10px 20px;
  margin: 10px;
  border-radius: 5px;
  cursor: pointer;
  transition: background 0.3s ease;
}

button:hover {
  background: #2ecc71;
}

#box {
  width: 100px;
  height: 100px;
  background: coral;
  margin: 20px auto;
  position: relative;
}

/* Keyframes animation */
@keyframes moveBox {
  0%   { transform: translateX(0); background: coral; }
  50%  { transform: translateX(200px); background: lightblue; }
  100% { transform: translateX(0); background: coral; }
}

script.js
// Function with parameters and return value
function calculateArea(length, width) {
  return length * width;
}

// Trigger CSS animation with JS
const animateBtn = document.getElementById("animateBtn");
const box = document.getElementById("box");

animateBtn.addEventListener("click", function() {
  // Restart animation
  box.style.animation = "none";
  void box.offsetWidth; // trigger reflow
  box.style.animation = "moveBox 2s ease-in-out";
});

// Handle form submission to calculate area
document.getElementById("areaForm").addEventListener("submit", function(e) {
  e.preventDefault();

  let length = parseFloat(document.getElementById("length").value);
  let width = parseFloat(document.getElementById("width").value);

  if (isNaN(length) || isNaN(width)) {
    document.getElementById("result").textContent = "Please enter valid numbers.";
    return;
  }

  let area = calculateArea(length, width);
  document.getElementById("result").textContent = `The area is ${area}.`;
});

