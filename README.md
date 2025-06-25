# 🌐 Animated Navigation Bar

This is a simple and modern **Animated Navigation Bar** built using **HTML**, **CSS**, and **JavaScript**. It features a responsive layout, smooth transitions, and an animated hamburger menu that toggles the navigation links with a stylish rotation effect.

---

## 🚀 Live Demo

You can see the animation in action by opening `index.html` in your browser.

> ✅ *You can also deploy it via GitHub Pages for live preview.*

---

## 📸 Preview



![Navigation Bar Open](https://github.com/user-attachments/assets/b36cb0b4-aaa4-4e7e-b216-8c6ca594a27e)


![Navigation Bar Close](https://github.com/user-attachments/assets/52011292-c470-4083-9220-6814a42db554)

---

## 🧾 Features

- 🔄 Smooth open/close animation
- 🍔 Hamburger menu with animated lines
- 🔁 Rotating navigation links on reveal
- 💻 Responsive and centered design
- ⚡ Lightweight and fast – no frameworks

---

## 🛠️ Technologies Used

- **HTML5** – Markup and structure
- **CSS3** – Styling and animation
- **Vanilla JavaScript** – Interactivity and toggle functionality

---

## 📂 Project Structure
animated-navigation-bar/
├── index.html       # Main HTML file
├── style.css        # Styling with animations and layout
└── script.js        # JavaScript for interactivity
---

---

## 💡 How It Works

The `#toggle` button toggles the `active` class on the `nav` element. This class triggers CSS transitions for expanding the menu and animating the links.


## Project Code:
### Html, CSS, JS Script:
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="style.css" />
    <title>Animated Navigation</title>
  </head>
  <body>
    <nav class="active" id="nav">
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Works</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
      <button class="icon" id="toggle">
        <div class="line line1"></div>
        <div class="line line2"></div>
      </button>
    </nav>
    <script src="script.js"></script>
  </body>
</html>
```

### CSS
```css
@import url("https://fonts.googleapis.com/css2?family=Muli&display=swap");

* {
  box-sizing: border-box;
}

body {
  background-color: #eafbff;
  background-image: linear-gradient(
    to bottom,
    #eafbff 0%,
    #eafbff 50%,
    #5290f9 50%,
    #5290f9 100%
  );
  font-family: "Muli", sans-serif;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
  margin: 0;
}

nav {
  background-color: #fff;
  padding: 20px;
  width: 80px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 3px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.3);
  transition: width 0.6s linear;
}

nav.active {
  width: 350px;
}

nav ul {
  display: flex;
  list-style-type: none;
  padding: 0;
  margin: 0;
  width: 0;
  transition: width 0.6s linear;
  overflow-x: hidden;
}

nav.active ul {
  width: 100%;
}

nav ul li {
  transform: rotateY(0deg);
  opacity: 0;
  transition: transform 0.6s linear, opacity 0.6s linear;
}

nav.active ul li {
  transform: rotateY(360deg);
  opacity: 1;
}

nav ul a {
  position: relative;
  color: #000;
  text-decoration: none;
  margin: 0 10px;
}

.icon {
  background-color: #fff;
  border: 0;
  cursor: pointer;
  padding: 0;
  position: relative;
  height: 30px;
  width: 30px;
}

.icon:focus {
  outline: 0;
}

.icon .line {
  background-color: #5290f9;
  height: 2px;
  width: 20px;
  position: absolute;
  top: 10px;
  left: 5px;
  transition: transform 0.6s linear;
}

.icon .line2 {
  top: auto;
  bottom: 10px;
}

nav.active .icon .line1 {
  transform: rotate(-765deg) translateY(5.5px);
}

nav.active .icon .line2 {
  transform: rotate(765deg) translateY(-5.5px);
}
```
### JS script 
```script
const toggle = document.getElementById("toggle");
const nav = document.getElementById("nav");

toggle.addEventListener("click", () => nav.classList.toggle("active"));

```
## Feedback 

Let me know if you'd like me to:
- Insert your **GitHub username or name**
- Add **real screenshots**
- Include a **live GitHub Pages link**

