<!DOCTYPE html>
<html>
<head>
    <title>Da Nang Moto Run</title>
    <style>
        body { margin: 0; overflow: hidden; background: #333; display: flex; justify-content: center; align-items: center; height: 100vh; font-family: Arial, sans-serif; }
        canvas { background: #87CEEB; border: 4px solid #fff; box-shadow: 0 0 20px rgba(0,0,0,0.5); }
    </style>
</head>
<body>
    <canvas id="gameCanvas"></canvas>

<script>
const canvas = document.getElementById('gameCanvas');
const ctx = canvas.getContext('2d');

// Настройки экрана
canvas.width = 800;
canvas.height = 400;

// Игровые переменные
let score = 0;
let gameSpeed = 5;
let isGameOver = false;

// Объект байка (игрок)
const bike = {
    x: 50,
    y: 300,
    width: 100,
    height: 60,
    dy: 0,
    jumpForce: 15,
    gravity: 0.8,
    isGrounded: false,
    color: 'black'
};

// Препятствия
const obstacles = [];
const obstacleTimer = 1500; // Появление каждые 1.5 сек
let lastTime = 0;

// Управление
window.addEventListener('keydown', (e) => {
    if (e.code === 'Space' && bike.isGrounded) {
        bike.dy = -bike.jumpForce;
        bike.isGrounded = false;
    }
    if (e.code === 'Space' && isGameOver) {
        location.reload(); // Перезагрузка при проигрыше
    }
});

function drawBike() {
    // Тело байка
    ctx.fillStyle = bike.color;
    ctx.fillRect(bike.x, bike.y, bike.width, bike.height);
    
    // Колеса
    ctx.fillStyle = "#333";
    ctx.beginPath();
    ctx.arc(bike.x + 20, bike.y + 60, 15, 0, Math.PI * 2);
    ctx.arc(bike.x + 80, bike.y + 60, 15, 0, Math.PI * 2);
    ctx.fill();

    // Заглушка для персонажей (водитель в комбинезоне и подруга в красной юбке)
    ctx.fillStyle = "blue"; // Водитель
    ctx.fillRect(bike.x + 40, bike.y - 30, 20, 40);
    ctx.fillStyle = "red";  // Подруга
    ctx.fillRect(bike.x + 15, bike.y - 25, 20, 35);
}

function spawnObstacle() {
    const types = ['люк', 'человек'];
    const type = types[Math.floor(Math.random() * types.length)];
    obstacles.push({
        x: canvas.width,
        y: 340,
        width: 40,
        height: 20,
        type: type,
        color: type === 'люк' ? '#444' : '#e0ac69'
    });
}

function update(time) {
    if (isGameOver) return;

    ctx.clearRect(0, 0, canvas.width, canvas.height);

    // Гравитация и прыжок
    bike.dy += bike.gravity;
    bike.y += bike.dy;

    if (bike.y > 300) {
        bike.y = 300;
        bike.dy = 0;
        bike.isGrounded = true;
    }

    // Отрисовка дороги
    ctx.fillStyle = "#777";
    ctx.fillRect(0, 360, canvas.width, 40);

    drawBike();

    // Работа с препятствиями
    if (time - lastTime > obstacleTimer) {
        spawnObstacle();
        lastTime = time;
    }

    for (let i = obstacles.length - 1; i >= 0; i--) {
        const o = obstacles[i];
        o.x -= gameSpeed;

        ctx.fillStyle = o.color;
        ctx.fillRect(o.x, o.y, o.width, o.height);

        // Проверка столкновения
        if (bike.x < o.x + o.width &&
            bike.x + bike.width > o.x &&
            bike.y < o.y + o.height &&
            bike.y + bike.height > o.y) {
            isGameOver = true;
        }

        if (o.x < -o.width) {
            obstacles.splice(i, 1);
            score++;
        }
    }

    // Очки
    ctx.fillStyle = "white";
    ctx.font = "20px Arial";
    ctx.fillText(`Очки: ${score}`, 20, 40);

    if (isGameOver) {
        ctx.fillStyle = "rgba(0,0,0,0.7)";
        ctx.fillRect(0, 0, canvas.width, canvas.height);
        ctx.fillStyle = "white";
        ctx.textAlign = "center";
        ctx.fillText("БАБАХ! Вы врезались!", canvas.width/2, canvas.height/2);
        ctx.fillText("Нажми ПРОБЕЛ, чтобы поехать снова", canvas.width/2, canvas.height/2 + 40);
    }

    requestAnimationFrame(update);
}

requestAnimationFrame(update);
</script>
</body>
</html>
