<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For Bauni Shri ji 💖</title>

<style>
  body {
    margin: 0;
    height: 100vh;
    font-family: 'Poppins', sans-serif;
    background: linear-gradient(135deg, #ffd6e8, #ffeef5);
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;
  }

  .card {
    background: white;
    padding: 35px;
    border-radius: 20px;
    text-align: center;
    box-shadow: 0 12px 30px rgba(0,0,0,0.2);
    width: 90%;
    max-width: 360px;
    position: relative;
  }

  h1 {
    color: #e91e63;
    margin-bottom: 10px;
  }

  p {
    color: #777;
    font-style: italic;
    font-size: 14px;
  }

  .buttons {
    margin-top: 25px;
    position: relative;
    height: 90px;
  }

  button {
    padding: 12px 26px;
    font-size: 16px;
    border-radius: 30px;
    border: none;
    cursor: pointer;
    transition: 0.2s ease;
  }

  #yes {
    background: #e91e63;
    color: white;
  }

  #no {
    background: #eee;
    color: #333;
    position: fixed;
    left: 50%;
    top: 55%;
    transform: translate(-50%, -50%);
  }

  .heart {
    position: absolute;
    font-size: 18px;
    animation: float 6s linear infinite;
    opacity: 0.7;
  }

  @keyframes float {
    from { transform: translateY(0); }
    to { transform: translateY(-800px); }
  }
</style>
</head>
<body>

<div class="card">
  <h1>❤️ Shri Ji ❤️</h1>
  <h2>Will you be my Valentine? and pay me 5 rupees daily?</h2>
  <p>“Every moment with you feels like a dream come true…”</p>

  <div class="buttons">
    <button id="yes">Yes 💖</button>
    <button id="no">No</button>
  </div>
</div>

<script>
  const noBtn = document.getElementById("no");
  const yesBtn = document.getElementById("yes");

  const messages = [
    "Are you sure? 😐",
    "Think again 🫠",
    "Please 🥺",
    "Don’t do this 😭",
    "Nice try 😏",
    "You know you want to 💘"
    "Oil up for diddy"
  ];
  let i = 0;

function moveNoButton() {
  const padding = 20;

  const maxX = window.innerWidth - noBtn.offsetWidth - padding;
  const maxY = window.innerHeight - noBtn.offsetHeight - padding;

  const x = Math.random() * maxX;
  const y = Math.random() * maxY;

  noBtn.style.left = x + "px";
  noBtn.style.top = y + "px";
  noBtn.innerText = messages[i % messages.length];
  i++;
}

  // Desktop
  noBtn.addEventListener("mouseover", moveNoButton);
  // Mobile
  noBtn.addEventListener("touchstart", moveNoButton);

  yesBtn.onclick = () => {
    document.body.innerHTML = `
      <div style="
        height:100vh;
        display:flex;
        flex-direction:column;
        align-items:center;
        justify-content:center;
        background:linear-gradient(135deg,#ffb6c1,#ffe4ec);
        font-family:Poppins,sans-serif;
        text-align:center;">
        <h1 style="color:#e91e63;">Shri ji said YES 💘</h1>
        <h2>Oil up u piglet nigga 🥰</h2>
      </div>
    `;
  };

  // Floating hearts
  setInterval(() => {
    const heart = document.createElement("div");
    heart.className = "heart";
    heart.innerText = "💗";
    heart.style.left = Math.random() * window.innerWidth + "px";
    heart.style.bottom = "0px";
    document.body.appendChild(heart);
    setTimeout(() => heart.remove(), 6000);
  }, 300);
</script>

</body>
</html>
