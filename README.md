<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Forever With You ❤️</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<!-- QR Code Library -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js"></script>

<style>
    body {
        margin: 0;
        height: 100vh;
        background: radial-gradient(circle at top, #ff9a9e, #fad0c4, #fad0c4);
        display: flex;
        justify-content: center;
        align-items: center;
        font-family: 'Segoe UI', sans-serif;
        overflow: hidden;
        color: white;
        text-align: center;
    }

    .container {
        background: rgba(255, 255, 255, 0.18);
        padding: 35px 25px;
        border-radius: 22px;
        box-shadow: 0 0 40px rgba(255, 0, 100, 0.4);
        backdrop-filter: blur(12px);
        max-width: 360px;
        animation: glow 3s infinite alternate;
    }

    @keyframes glow {
        from { box-shadow: 0 0 20px rgba(255, 0, 100, 0.3); }
        to { box-shadow: 0 0 45px rgba(255, 0, 100, 0.7); }
    }

    h1 {
        font-size: 30px;
        margin-bottom: 10px;
    }

    p {
        font-size: 16px;
        line-height: 1.6;
        margin-bottom: 22px;
    }

    #qrcode {
        background: white;
        padding: 14px;
        border-radius: 14px;
        display: inline-block;
    }

    .hint {
        margin-top: 16px;
        font-size: 14px;
        opacity: 0.9;
    }

    /* Floating hearts */
    .heart {
        position: absolute;
        color: rgba(255, 255, 255, 0.7);
        animation: float 7s linear infinite;
        user-select: none;
    }

    @keyframes float {
        0% {
            transform: translateY(100vh) scale(0.7);
            opacity: 0;
        }
        20% {
            opacity: 1;
        }
        100% {
            transform: translateY(-10vh) scale(1.3);
            opacity: 0;
        }
    }
</style>
</head>
<body>

<!-- 🎶 Background Music -->
<audio autoplay loop>
    <source src="https://cdn.pixabay.com/audio/2022/10/16/audio_7c48f3cbd4.mp3" type="audio/mpeg">
</audio>

<div class="container">
    <h1>Hey My Love ❤️</h1>
    <p>
        This QR code isn’t just pixels…  
        It’s a piece of my heart,  
        something I’ve been wanting to say to you.
    </p>

    <div id="qrcode"></div>

    <div class="hint">📱 Scan this with your heart</div>
</div>

<script>
    // 💖 CHANGE HER NAME HERE
    const herName = "My Love";

    const loveMessage = `
Hey ${herName} ❤️,

I don’t know when it started,
but somewhere between our talks, smiles,
and silent moments,
you became my favorite thought.

You make ordinary days feel special
and special days unforgettable.

I don’t promise a perfect life,
but I promise a real one —
with loyalty, care, respect,
and a heart that will always choose you.

So here I am, honestly and fearlessly asking…

Will you hold my hand,
walk with me through every season of life,
and be mine today, tomorrow,
and forever? 💍❤️

— Saransh
    `;

    new QRCode(document.getElementById("qrcode"), {
        text: loveMessage,
        width: 190,
        height: 190
    });

    // Floating hearts creation
    for (let i = 0; i < 30; i++) {
        let heart = document.createElement("div");
        heart.className = "heart";
        heart.innerHTML = "❤️";
        heart.style.left = Math.random() * 100 + "vw";
        heart.style.fontSize = (18 + Math.random() * 22) + "px";
        heart.style.animationDuration = (4 + Math.random() * 5) + "s";
        document.body.appendChild(heart);
    }
</script>

</body>
</html>
