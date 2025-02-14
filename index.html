const canvas = document.getElementById("gameCanvas");
const ctx = canvas.getContext("2d");

canvas.width = 400;
canvas.height = 500;

const player = {
    x: 180,
    y: 450,
    width: 40,
    height: 20,
    color: "white",
    speed: 5,
    bullets: []
};

const enemies = [];
const enemyRow = 3;
const enemyCol = 6;
const enemyWidth = 30;
const enemyHeight = 20;
const enemySpacing = 10;
const enemySpeed = 1;

for (let row = 0; row < enemyRow; row++) {
    for (let col = 0; col < enemyCol; col++) {
        enemies.push({
            x: col * (enemyWidth + enemySpacing) + 50,
            y: row * (enemyHeight + enemySpacing) + 30,
            width: enemyWidth,
            height: enemyHeight,
            color: "red"
        });
    }
}

let rightPressed = false;
let leftPressed = false;

document.addEventListener("keydown", (event) => {
    if (event.key === "ArrowRight") rightPressed = true;
    if (event.key === "ArrowLeft") leftPressed = true;
    if (event.key === " "){
        player.bullets.push({ x: player.x + player.width / 2 - 2, y: player.y, width: 4, height: 10 });
    }
});

document.addEventListener("keyup", (event) => {
    if (event.key === "ArrowRight") rightPressed = false;
    if (event.key === "ArrowLeft") leftPressed = false;
});

function update() {
    if (rightPressed && player.x + player.width < canvas.width) player.x += player.speed;
    if (leftPressed && player.x > 0) player.x -= player.speed;

    player.bullets.forEach((bullet, index) => {
        bullet.y -= 5;
        if (bullet.y < 0) player.bullets.splice(index, 1);
    });

    enemies.forEach((enemy, eIndex) => {
        enemy.x += enemySpeed;
        if (enemy.x + enemy.width > canvas.width || enemy.x < 0) {
            enemies.forEach(e => e.x -= enemySpeed * 2);
        }
        player.bullets.forEach((bullet, bIndex) => {
            if (
                bullet.x < enemy.x + enemy.width &&
                bullet.x + bullet.width > enemy.x &&
                bullet.y < enemy.y + enemy.height &&
                bullet.y + bullet.height > enemy.y
            ) {
                enemies.splice(eIndex, 1);
                player.bullets.splice(bIndex, 1);
            }
        });
    });
}

function draw() {
    ctx.clearRect(0, 0, canvas.width, canvas.height);

    ctx.fillStyle = player.color;
    ctx.fillRect(player.x, player.y, player.width, player.height);

    player.bullets.forEach((bullet) => {
        ctx.fillStyle = "yellow";
        ctx.fillRect(bullet.x, bullet.y, bullet.width, bullet.height);
    });

    enemies.forEach((enemy) => {
        ctx.fillStyle = enemy.color;
        ctx.fillRect(enemy.x, enemy.y, enemy.width, enemy.height);
    });
}

function gameLoop() {
    update();
    draw();
    requestAnimationFrame(gameLoop);
}

gameLoop();
