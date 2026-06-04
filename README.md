<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Our Friendship 🌸</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial, sans-serif;
}

body{
    min-height:100vh;
    background:linear-gradient(135deg,#ffd6e7,#ffe8c7);
    text-align:center;
    overflow-x:hidden;
}

header{
    padding:40px 20px;
}

h1{
    color:#ff4d88;
    font-size:3rem;
}

.subtitle{
    margin-top:10px;
    font-size:1.2rem;
}

#friendshipCounter{
    margin-top:20px;
    font-size:1.3rem;
    font-weight:bold;
    color:#ff4d88;
}

.buttons{
    display:flex;
    flex-wrap:wrap;
    justify-content:center;
    gap:15px;
    margin:20px;
}

button{
    padding:14px 24px;
    border:none;
    border-radius:30px;
    background:#ff4d88;
    color:white;
    cursor:pointer;
    font-size:1rem;
    transition:0.3s;
}

button:hover{
    transform:scale(1.08);
}

.content{
    max-width:850px;
    margin:auto;
    padding:20px;
}

.card{
    background:rgba(255,255,255,0.8);
    backdrop-filter:blur(10px);
    padding:25px;
    border-radius:20px;
    box-shadow:0 10px 30px rgba(0,0,0,0.1);
    animation:fade 0.5s ease;
}

img{
    max-width:100%;
    border-radius:15px;
    margin-top:15px;
}

footer{
    margin-top:40px;
    padding:20px;
}

@keyframes fade{
    from{
        opacity:0;
        transform:translateY(20px);
    }
    to{
        opacity:1;
        transform:translateY(0);
    }
}

.heart{
    position:fixed;
    bottom:-20px;
    animation:float 6s linear infinite;
    font-size:20px;
    opacity:0.7;
}

@keyframes float{
    0%{
        transform:translateY(0);
        opacity:0.7;
    }
    100%{
        transform:translateY(-110vh);
        opacity:0;
    }
}
</style>
</head>

<body>

<header>
<h1>🌸 Welcome 🌸</h1>

<p class="subtitle">
A tiny corner of the internet dedicated to an amazing friend.
</p>

<div id="friendshipCounter"></div>
</header>

<div class="buttons">
<button onclick="showMemory()">📸 Memory Lane</button>
<button onclick="showFunny()">😂 Funny Zone</button>
<button onclick="showAppreciation()">🌟 Appreciation</button>
<button onclick="showCompliment()">💌 Compliment</button>
<button onclick="showReasons()">❤️ Why You're Awesome</button>
<button onclick="showGallery()">🖼 Gallery</button>
<button onclick="toggleMusic()">🎵 Music</button>
<button onclick="showFinal()">🎁 Final Surprise</button>
</div>

<div class="content" id="content">
<div class="card">
<h2>✨ Click any button above ✨</h2>
<p>And explore our friendship universe.</p>
</div>
</div>

<audio id="bgMusic" loop>
<source src="your-song.mp3" type="audio/mpeg">
</audio>

<footer>
Made with memories, friendship and lots of smiles ❤️
</footer>

<script>

// ========= FRIENDSHIP COUNTER =========
// CHANGE THIS DATE

const friendshipDate = new Date("2025-01-01");

function updateCounter(){

const today = new Date();

const diff =
today.getTime() - friendshipDate.getTime();

const days =
Math.floor(diff/(1000*60*60*24));

document.getElementById("friendshipCounter")
.innerHTML =
`🌸 Friends for ${days} beautiful days 🌸`;
}

updateCounter();


// ========= MUSIC =========

let musicPlaying = false;

function toggleMusic(){

const music =
document.getElementById("bgMusic");

if(!musicPlaying){
music.play();
musicPlaying = true;
}
else{
music.pause();
musicPlaying = false;
}
}


// ========= COMPLIMENTS =========

const compliments = [
"You're one of the kindest people I know.",
"Your laugh is contagious.",
"You make ordinary days memorable.",
"You're genuinely special.",
"Life feels lighter around you.",
"You deserve all the happiness.",
"You are amazing exactly as you are."
];


// ========= REASONS =========

const reasons = [
"Because you're always there.",
"Because you make people smile.",
"Because you care deeply.",
"Because your energy is unmatched.",
"Because you're unforgettable.",
"Because friendship with you is a gift."
];


// ========= BUTTON FUNCTIONS =========

function showMemory(){

document.getElementById("content").innerHTML=`
<div class="card">
<h2>📸 Memory Lane</h2>

<p>
Add your favorite memory here.
</p>

<img src="photo1.jpg">

<p>
Replace photo1.jpg with your image.
</p>

</div>`;
}

function showFunny(){

document.getElementById("content").innerHTML=`
<div class="card">

<h2>😂 Funny Zone</h2>

<p>
Add your inside jokes here.
</p>

<ul style="text-align:left;margin-top:15px;">
<li>Funny Moment #1</li>
<li>Funny Moment #2</li>
<li>Funny Moment #3</li>
</ul>

</div>`;
}

function showAppreciation(){

document.getElementById("content").innerHTML=`
<div class="card">

<h2>🌟 Things I Appreciate About You</h2>

<p>✨ Your kindness</p>
<p>✨ Your sense of humor</p>
<p>✨ Your positivity</p>
<p>✨ Your support</p>
<p>✨ Just being yourself</p>

</div>`;
}

function showCompliment(){

let random =
compliments[Math.floor(Math.random()*compliments.length)];

document.getElementById("content").innerHTML=`
<div class="card">
<h2>💌 Random Compliment</h2>
<h3>${random}</h3>
</div>`;
}

function showReasons(){

let random =
reasons[Math.floor(Math.random()*reasons.length)];

document.getElementById("content").innerHTML=`
<div class="card">
<h2>❤️ Why You're Awesome</h2>
<h3>${random}</h3>
</div>`;
}

function showGallery(){

document.getElementById("content").innerHTML=`
<div class="card">

<h2>🖼 Friendship Gallery</h2>

<img src="photo1.jpg">
<img src="photo2.jpg">
<img src="photo3.jpg">

<p>
Replace with your own images.
</p>

</div>`;
}

function showFinal(){

document.getElementById("content").innerHTML=`
<div class="card">

<h2>🎁 Final Surprise 🎁</h2>

<p>
Thank you for all the laughs,
the memories,
the random conversations,
and every moment that made life a little brighter.
</p>

<br>

<p>
No matter where life takes us,
I hope we continue making memories,
sharing jokes,
and annoying each other forever.
</p>

<br>

<h3>
❤️ Premium Best Friend Membership Activated ❤️
</h3>

<br>

<p>
Valid until the end of the universe.
No cancellation allowed.
😌✨
</p>

<img src="final-photo.jpg">

</div>`;
}


// ========= FLOATING HEARTS =========

function createHeart(){

const heart =
document.createElement("div");

heart.classList.add("heart");

heart.innerHTML = "❤️";

heart.style.left =
Math.random()*100 + "vw";

heart.style.fontSize =
Math.random()*20 + 15 + "px";

document.body.appendChild(heart);

setTimeout(()=>{
heart.remove();
},6000);
}

setInterval(createHeart,700);

</script>

</body>
</html>
