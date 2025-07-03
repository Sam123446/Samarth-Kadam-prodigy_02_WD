let startTime, elapsedTime = 0, timerInterval;
let running = false;

function startTimer() {
    if (!running) {
        startTime = Date.now() - elapsedTime;
        timerInterval = setInterval(updateDisplay, 100);
        running = true;
    }
}

function pauseTimer() {
    if (running) {
        clearInterval(timerInterval);
        elapsedTime = Date.now() - startTime;
        running = false;
    }
}

function resetTimer() {
    clearInterval(timerInterval);
    elapsedTime = 0;
    running = false;
    document.getElementById("display").innerText = "00:00:00";
    document.getElementById("laps").innerHTML = "";
}

function recordLap() {
    if (running) {
        let lapTime = document.getElementById("display").innerText;
        let lapItem = document.createElement("li");
        lapItem.innerText = `Lap: ${lapTime}`;
        document.getElementById("laps").appendChild(lapItem);
    }
}

function updateDisplay() {
    let time = Date.now() - startTime;
    let seconds = Math.floor((time / 1000) % 60);
    let minutes = Math.floor((time / 60000) % 60);
    let hours = Math.floor(time / 3600000);

    document.getElementById("display").innerText =
        `${String(hours).padStart(2, '0')}:${String(minutes).padStart(2, '0')}:${String(seconds).padStart(2, '0')}`;
}
