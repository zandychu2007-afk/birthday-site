<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Happy Birthday</title>

<style>
body {
  margin: 0;
  height: 100vh;
  background: linear-gradient(to top, #ff9a9e, #fad0c4);
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
  font-family: 'Arial', sans-serif;
}

/* Title */
h1 {
  position: absolute;
  top: 50px;
  font-size: 3rem;
  color: white;
  text-shadow: 0 0 10px #fff, 0 0 20px #ff69b4;
  animation: glow 2s infinite alternate;
}

@keyframes glow {
  from { text-shadow: 0 0 10px #fff; }
  to { text-shadow: 0 0 30px #ff1493; }
}

/* Balloons */
.balloon {
  position: absolute;
  bottom: -150px;
  width: 50px;
  height: 70px;
  border-radius: 50%;
  animation: float 6s infinite ease-in;
}

.balloon::after {
  content: "";
  position: absolute;
  width: 2px;
  height: 40px;
  background: white;
  left: 50%;
  top: 70px;
}

@keyframes float {
  0% { transform: translateY(0); opacity: 1; }
  100% { transform: translateY(-110vh); opacity: 0; }
}

/* Different colors */
.balloon:nth-child(1) { left: 10%; background: red; animation-delay: 0s; }
.balloon:nth-child(2) { left: 30%; background: blue; animation-delay: 2s; }
.balloon:nth-child(3) { left: 50%; background: yellow; animation-delay: 4s; }
.balloon:nth-child(4) { left: 70%; background: green; animation-delay: 1s; }
.balloon:nth-child(5) { left: 90%; background: purple; animation-delay: 3s; }

/* Cake */
.cake {
  position: relative;
  width: 120px;
  height: 100px;
  background: #ff69b4;
  border-radius: 10px;
}

.cake::before {
  content: "";
  position: absolute;
  width: 120px;
  height: 30px;
  background: #fff;
  top: -30px;
  border-radius: 10px;
}

.candle {
  position: absolute;
  width: 10px;
  height: 30px;
  background: #fff;
  top: -60px;
  left: 50%;
  transform: translateX(-50%);
}

.flame {
  position: absolute;
  width: 10px;
  height: 10px;
  background: orange;
  border-radius: 50%;
  top: -10px;
  left: 50%;
  transform: translateX(-50%);
  animation: flicker 0.3s infinite;
}

@keyframes flicker {
  0% { transform: translateX(-50%) scale(1); }
  50% { transform: translateX(-50%) scale(1.2); }
  100% { transform: translateX(-50%) scale(1); }
}
</style>

</head>
<body>

<h1>🎉 Happy Birthday! 🎂</h1>

<div class="cake">
  <div class="candle">
    <div class="flame"></div>
  </div>
</div>

<!-- Balloons -->
<div class="balloon"></div>
<div class="balloon"></div>
<div class="balloon"></div>
<div class="balloon"></div>
<div class="balloon"></div>

</body>
</html>
