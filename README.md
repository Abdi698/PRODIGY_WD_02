myStopwatch
A simple and visually appealing stopwatch application built using HTML, CSS, and JavaScript.

Features
Start, Pause, and Reset: Control the stopwatch with intuitive buttons.
Lap Recording: Record and display lap times with the ability to delete individual laps.
Responsive Design: Ensures a great user experience on both desktop and mobile devices.
Custom Styling: Attractive design with background images, shadows, and animations.
Usage
Start: Click the "Start" button to begin the stopwatch.
Pause: Click the "Pause" button to pause the stopwatch.
Reset: Click the "Reset" button to reset the stopwatch to 00:00:00.
Lap: Click the "Lap" button to record the current time. Laps will be displayed below the buttons with an option to delete each lap.
Code Overview
HTML
The HTML structure includes a heading, a container for the stopwatch display, control buttons, and a list to display lap times.

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Stopwatch</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1>Stopwatch</h1>
    <div class="hero">
        <div class="counter">00:00:00</div>
        <button onclick="startStopwatch()">Start</button>
        <button onclick="pauseStopwatch()">Pause</button>
        <button onclick="resetStopwatch()">Reset</button>
        <button onclick="recordLap()">Lap</button>
    </div>
    <ul id="laps"></ul>
    <script src="script.js"></script>
</body>
</html>
CSS
The CSS provides styling for the body, heading, buttons, and lap list to create an attractive and responsive design.

body {
    font-family: 'Arial', sans-serif;
    text-align: center;
    margin: 50px;
    background-image: url("bg.jpg");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    color: #fff;
}

h1 {
    font-size: 3em;
    margin-bottom: 20px;
    color: #1eff00;
    text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
}

.hero {
    display: inline-block;
    padding: 20px;
    border-radius: 15px;
    background: url('watchbg.jpg') no-repeat center center;
    background-size: cover;
    box-shadow: 0px 0px 15px rgba(255, 255, 255, 0.3);
}

.counter {
    font-size: 2.5em;
    margin: 20px auto;
    padding: 15px;
    width: 300px;
    border-radius: 15px;
    border: 2px solid #fff;
    background: rgba(0, 0, 0, 0.6);
    color: #0bf517;
    box-shadow: 0px 0px 10px rgba(255, 255, 255, 0.3);
}

button {
    font-size: 1.2em;
    margin: 10px;
    padding: 10px 20px;
    cursor: pointer;
    border: none;
    border-radius: 10px;
    background: linear-gradient(45deg, #00c6ff, #0072ff);
    color: white;
    transition: 0.3s;
}

button:hover {
    background: linear-gradient(45deg, #ff00f2, #00c6ff);
    transform: scale(1.05);
}

ul {
    list-style: none;
    padding: 0;
}

li {
    font-size: 1.5em;
    padding: 10px;
    border-radius: 10px;
    border: 1px solid #d4cece;
    background-color: rgba(255, 255, 255, 0.2);
    margin: 5px auto;
    width: 250px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.erase-btn {
    font-size: 0.8em;
    padding: 5px 10px;
    background: rgb(255, 4, 4);
    color: rgb(206, 189, 189);
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

.erase-btn:hover {
    background: rgb(221, 85, 85);
}

@media (max-width: 768px) {
    .hero {
        width: 90%;
    }
}
JavaScript
The JavaScript handles the stopwatch functionality, including starting, pausing, resetting, and recording lap times.

let timer;
let startTime;
let elapsedTime = 0;
let running = false;

function update() {
    const time = Date.now() - startTime + elapsedTime;
    const seconds = Math.floor((time / 1000) % 60);
    const minutes = Math.floor((time / 1000 / 60) % 60);
    const hours = Math.floor(time / 1000 / 60 / 60);
    document.querySelector = lapTime;

        const deleteButton = document.createElement("button");
        deleteButton.textContent = "X";
        deleteButton.classList.add("erase-btn");
        deleteButton.onclick = function () {
            lapItem.remove();
        };

        lapItem.appendChild(deleteButton);
        document.getElementById("laps").appendChild(lapItem);
    }
}
Installation
Clone the repository:
git clone https://github.com/Abdi698/myStopwatch.git
Navigate to the project directory:
cd myStopwatch
Open myStopwatch.html in your preferred web browser.
Contributing
Feel free to submit issues or pull requests. Contributions are welcome!

License
This project is licensed under the MIT License.
