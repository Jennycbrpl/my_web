<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Jenny | AI Baby Engineer ✨</title>

<style>
/* ====== RESET ====== */
*{margin:0;padding:0;box-sizing:border-box;font-family:"Poppins",sans-serif;}

/* ===== BACKGROUND GALAXY ===== */
body{
background: radial-gradient(circle at 10% 10%,#1b002f,#000 60%);
color:#fff;min-height:100vh;overflow-x:hidden;
display:flex;flex-direction:column;align-items:center;
}

.glow{
position: fixed;
width:600px;height:600px;
background:rgba(153,0,255,0.12);
filter:blur(130px);
border-radius:50%;
top:-150px;right:-200px;z-index:-1;
}

/* ===== HEADER TYPEWRITER ===== */
header{margin-top:3rem;text-align:center;}
.typewriter{
font-size:2rem;font-weight:600;border-right:3px solid #fff;
white-space:nowrap;overflow:hidden;width:0;
animation:typing 3s steps(30,end) forwards,blink .8s infinite;
}

@keyframes typing{from{width:0;}to{width:100%;}}
@keyframes blink{50%{border-color:transparent;}}

/* ===== CARD SECTIONS ===== */
section{
width:85%;max-width:900px;margin:2rem auto;
padding:2rem;background:rgba(255,255,255,0.05);
backdrop-filter:blur(12px);border:1px solid rgba(255,255,255,0.1);
border-radius:20px;box-shadow:0 0 20px rgba(255,255,255,0.07);
}

/* ===== TITLES ===== */
h2{
font-size:1.8rem;margin-bottom:1rem;
background:linear-gradient(90deg,#cd7cff,#7afcff);
-webkit-background-clip:text;color:transparent;
}

/* ===== PROFILE IMG ===== */
main img{
max-width:230px;border-radius:20px;margin:1rem;
box-shadow:0 0 30px rgba(255,255,255,0.2);
transition:0.3s;
}
main img:hover{transform:scale(1.05);}

/* ===== LIST STYLES ===== */
li{margin:0.4rem 0;}

/* ===== BADGES ===== */
.badge{
display:inline-block;margin:5px;padding:8px 14px;
background:#15002a;border:1px solid #9e4aff;
border-radius:12px;font-size:0.9rem;
}

/* ===== PROGRESS BAR ===== */
.level-container{margin:8px 0;}
.level{height:10px;width:100%;background:#2a2a3e;border-radius:10px;}
.fill{
height:100%;background:linear-gradient(90deg,#a855f7,#22d3ee);
border-radius:10px;
}

/* ===== FOOTER ===== */
footer{margin:2rem 0;font-size:0.9rem;opacity:0.7;}
a{color:#9e65ff;text-decoration:none;}
a:hover{text-decoration:underline;}
</style>
</head>

<body>
<div class="glow"></div>

<header><div id="typewriter" class="typewriter"></div></header>

<main>
<img src="foto2jpg.jpg">
<img src="fotoJenny.jpg">
</main>

<section>
<h2>🌸 About me</h2>
<p>✨ Pre-uni tech girl building her future in AI & software</p>
<ul>
<li>📚 Future AI researcher</li>
<li>💻 Ingeniería informática vibes</li>
<li>🌐 Idiomas enjoyer (EN / JP / DE / ES / Quechua beginner)</li>
<li>🐶 Puppies lover + running freak</li>
<li>🤍 Sueño: crear tech con impacto real</li>
</ul>
</section>

<section>
<h2>⚙️ Tech Stack</h2>
<div>
<span class="badge">Python</span>
<span class="badge">HTML</span>
<span class="badge">CSS</span>
<span class="badge">JavaScript</span>
<span class="badge">Git & GitHub</span>
</div>

<div class="level-container">Python
<div class="level"><div class="fill" style="width:70%"></div></div></div>

<div class="level-container">Web Dev
<div class="level"><div class="fill" style="width:55%"></div></div></div>

<div class="level-container">AI / ML learning path
<div class="level"><div class="fill" style="width:25%"></div></div></div>
</section>

<section>
<h2>🕒 Timeline</h2>
<ul>
<li>2023 — Me gradué con el 1° puesto</li>
<li>2024 — Becada en dos programas tech</li>
<li>2025 — Primera web personal + hackathon + Harvard CS50</li>
<li>2026 — AI dream loading…</li>
</ul>
</section>

<section>
<h2>🚀 Projects</h2>
<ul>
<li>✅ Web personal</li>
<li>✅ Prototipo de app para gente discapacitada en Figma</li>
<li>✅ Proyecto eco-vegan product concept</li>
<li>📚 Harvard CS50 progress</li>
</ul>
</section>

<section>
<h2>🌈 Random facts</h2>
<ul>
<li>🧠 Me gusta aprender idiomas</li>
<li>🏃‍♀️ Me gusta el running </li>
<li>👾 Chess player</li>
<li>🤝 Me encanta conocer gente creativa</li>
</ul>
</section>

<section>
<h2>🎯 Metas 2025</h2>
<ul>
<li>Crear un club tech</li>
<li>Crear mi primer mini-proyecto de IA</li>
<li></li>
</ul>
</section>

<section style="text-align:center;">
<h2>📬 Contact</h2>
<a href="mailto:jennycabrerapalomino1@gmail.com">Email me 💫</a><br>
</section>

<footer>Handmade with 💜 by Jenny © 2025</footer>

<script>
const frases=[
"✨ Hola, soy Jenny",
"🌐 Hello, I’m Jenny",
"🇯🇵 こんにちは、ジェニーです",
"🇩🇪 Hallo, ich bin Jenny",
"🌎 Ñuqaqa Jenny kani",
"💫 Future AI Engineer",
"👾 Coding + idiomas + ciencia"
];
let i=0;
const el=document.getElementById("typewriter");
function type(){
el.textContent="";el.style.width="0";
let t=0;let int=setInterval(()=>{
if(t<frases[i].length){el.textContent+=frases[i][t];t++;}else{
clearInterval(int);setTimeout(()=>del(),1500);}
},120);}
function del(){setTimeout(()=>{
i=(i+1)%frases.length;type();document.title=frases[i];
},2000);}
type();
</script>

</body>
</html>
