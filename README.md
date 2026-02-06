<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Valentine 💖</title>

<style>
body {
    margin: 0;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #ffe6eb;
    font-family: Arial, sans-serif;
}

.container {
    background: white;
    padding: 30px;
    border-radius: 15px;
    text-align: center;
    position: relative;
    width: 300px;
}

button {
    padding: 10px 20px;
    font-size: 16px;
    border: none;
    border-radius: 8px;
    cursor: pointer;
}

#yes {
    background-color: #ff4d6d;
    color: white;
}

#no {
    background-color: gray;
    color: white;
    position: absolute;
}
</style>
</head>

<body>

<div class="container">
    <h2>Will you be my Valentine? 💘</h2>
    <button id="yes" onclick="yesClicked()">Yes 💖</button>
    <button id="no">No 🙄</button>
</div>

<script>
const noBtn = document.getElementById("no");

noBtn.addEventListener("mouseenter", moveButton);

function moveButton() {
    const container = document.querySelector(".container");

    const maxX = container.clientWidth - noBtn.offsetWidth;
    const maxY = container.clientHeight - noBtn.offsetHeight;

    const x = Math.random() * maxX;
    const y = Math.random() * maxY;

    noBtn.style.left = x + "px";
    noBtn.style.top = y + "px";
}

function yesClicked() {
    document.body.innerHTML = "<h1 style='color:#ff4d6d;'>YAY 💕 I knew it 😍</h1>";
}
</script>

</body>
</html>
