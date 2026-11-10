<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Brooklane Aranca | Portfolio</title>

<style>
*{margin:0;padding:0;box-sizing:border-box}
html,body{width:100%;height:100%;overflow:hidden;background:#080808;color:#f5f5f5;font-family:Arial,Helvetica,sans-serif}

.page{position:absolute;inset:0;width:100%;height:100vh;height:100dvh;display:none;flex-direction:column;overflow:hidden}
.page.active{display:flex}

nav{height:55px;min-height:55px;display:flex;justify-content:space-between;align-items:center;border-bottom:1px solid #292929;gap:12px}
.logo{font-size:12px;font-weight:bold;letter-spacing:1.5px;white-space:nowrap}
.logo span{color:#777}
.nav-links{display:flex;gap:15px;align-items:center}
.nav-links button{background:none;border:none;color:#999;font-size:9px;letter-spacing:1px;cursor:pointer;font-family:Arial,sans-serif}
.nav-links button:hover{color:white}

.binary-rain{position:absolute;inset:0;overflow:hidden;pointer-events:none;z-index:0;opacity:.13}
.binary-rain span{position:absolute;color:#fff;font-family:monospace;font-size:12px;line-height:2;white-space:pre;animation:rain 12s linear infinite}
@keyframes rain{from{transform:translateY(0)}to{transform:translateY(200vh)}}

.page-btn{background:transparent;color:#ddd;border:1px solid #777;padding:11px 20px;font-size:9px;letter-spacing:2px;cursor:pointer;transition:.3s;font-family:Arial,sans-serif}
.page-btn:hover{background:#eee;color:#080808}

.bottom,.page2-footer,.page3-footer,.page4-footer{border-top:1px solid #292929;display:flex;justify-content:space-between;align-items:center;gap:10px;color:#777;font-size:9px;letter-spacing:2px}
.bottom{min-height:35px}
.page2-footer,.page3-footer,.page4-footer{padding-top:10px}

/* PAGE 1 */
#page1{padding:22px 6%}
.page1-content{position:relative;z-index:1;height:100%;display:flex;flex-direction:column;min-height:0}
.hero{flex:1;min-height:0;display:flex;align-items:center;justify-content:space-between;gap:45px}
.hero-text{flex:1;min-width:0}
.tag{color:#888;font-size:10px;letter-spacing:4px;margin-bottom:20px}
.hero h1{font-size:clamp(34px,5.5vw,68px);line-height:1.05;letter-spacing:-2px;margin-bottom:20px}
.hero h1 span,.page3-heading h1 span{color:#888}
.subtitle{font-size:clamp(13px,1.5vw,17px);color:#ccc;margin-bottom:20px;letter-spacing:1px}
.description{max-width:510px;font-size:13px;line-height:1.9;color:#999}
.student-info{margin-top:22px;border-left:2px solid #666;padding-left:15px;color:#aaa;font-size:12px;line-height:2}
.next-area{margin-top:22px}
.photo-area{width:270px;height:350px;flex-shrink:0;position:relative;padding:9px;border:1px solid #444}
.photo-area img{width:100%;height:100%;object-fit:cover;filter:grayscale(20%)}
.photo-area:before,.photo-area:after{content:"";position:absolute;width:45px;height:45px;pointer-events:none}
.photo-area:before{top:-7px;left:-7px;border-top:2px solid #eee;border-left:2px solid #eee}
.photo-area:after{bottom:-7px;right:-7px;border-bottom:2px solid #eee;border-right:2px solid #eee}

/* PAGE 2 */
#page2{padding:22px 5%}
.page2-content{position:relative;z-index:1;width:min(1100px,100%);height:100%;min-height:0;margin:auto;display:flex;flex-direction:column;justify-content:space-between}
.page2-hero{text-align:center;padding:15px 0}
.page2-hero .subtitle{font-size:12px;letter-spacing:5px;color:#aaa;margin-bottom:14px}
.page2-hero h1{font-size:clamp(30px,5vw,45px);letter-spacing:2px;margin-bottom:12px}
.page2-hero>p{color:#bbb;font-size:14px;line-height:1.6}
.personal-details{display:flex;justify-content:center;flex-wrap:wrap;gap:10px 25px;margin-top:15px;color:#aaa;font-size:10px;letter-spacing:1px}
.page2-main{display:grid;grid-template-columns:1fr 1fr;gap:20px 45px;align-content:center}
.page2-main section h2{font-size:16px;letter-spacing:3px;text-transform:uppercase;margin-bottom:10px;padding-bottom:7px;border-bottom:1px solid #777}
.page2-main section p{color:#ccc;font-size:12px;line-height:1.55;text-align:justify}
.skills-list{margin:10px 0}
.skills-list p{text-align:left!important;margin-bottom:5px;color:#fff!important}
.education{grid-column:1/-1}
.education-list{display:grid;grid-template-columns:repeat(3,1fr);gap:22px}
.education-item{border-left:1px solid #888;padding-left:12px}
.education-item .year{color:#aaa;font-size:10px;letter-spacing:2px;margin-bottom:5px}
.education-item h3{font-size:13px;margin-bottom:5px}
.education-item p{text-align:left!important;font-size:11px!important;line-height:1.5!important}

/* PAGE 3 */
#page3{padding:22px 6%}
.page3-content{position:relative;z-index:1;height:100%;min-height:0;display:flex;flex-direction:column}
.page3-main{flex:1;min-height:0;display:flex;flex-direction:column;justify-content:center}
.page3-heading{margin-bottom:22px}
.page3-heading .tag{margin-bottom:12px}
.page3-heading h1{font-size:clamp(32px,5vw,58px);letter-spacing:-1px;margin-bottom:9px}
.page3-heading p{color:#aaa;font-size:13px;letter-spacing:1px}
.achievement-list{display:grid;grid-template-columns:1fr 1fr;gap:20px 42px}
.achievement-item{border-left:2px solid #666;padding:2px 0 2px 15px}
.achievement-item .date{color:#888;font-size:10px;letter-spacing:2px;margin-bottom:7px;text-transform:uppercase}
.achievement-item h2{font-size:15px;letter-spacing:1px;margin-bottom:6px}
.achievement-item p{color:#aaa;font-size:12px;line-height:1.6}

/* PAGE 4: FAMILY AND FRIENDS */
#page4{padding:18px 5%;position:relative}
.page4-content{position:relative;z-index:1;height:100%;min-height:0;display:flex;flex-direction:column}
.page4-heading{text-align:center;padding:10px 0 14px;flex-shrink:0}
.page4-heading .tag{margin-bottom:8px}
.page4-heading h1{font-size:clamp(28px,4vw,45px);letter-spacing:2px;margin-bottom:7px}
.page4-heading h1 span{color:#888}
.page4-heading p{font-size:12px;color:#aaa;letter-spacing:1px}

/* DARKER BINARY HEART BACKGROUND */
.binary-heart{
position:absolute;
inset:0;
display:grid;
grid-template-columns:repeat(41,15px);
grid-auto-rows:16px;
gap:1px;
place-content:center;
pointer-events:none;
z-index:0;
opacity:.09;
}

.binary-heart span{
color:#999;
font-family:monospace;
font-size:11px;
font-weight:normal;
text-align:center;
text-shadow:none;
}

/* FAMILY PROFILES */
.family-grid{
flex:1;
min-height:0;
display:grid;
grid-template-rows:1fr 1fr;
gap:12px;
align-content:center;
padding:4px 0;
}

.profile-pair{
width:100%;
min-height:0;
display:grid;
grid-template-columns:repeat(2,minmax(0,1fr));
gap:16px;
align-items:stretch;
}

.family-card{
min-width:0;
min-height:0;
display:grid;
grid-template-columns:minmax(95px,125px) minmax(0,1fr);
grid-template-rows:auto auto auto auto auto;
align-content:center;
align-items:center;
column-gap:15px;
row-gap:5px;
text-align:left;
padding:9px 12px;
border-left:1px solid #555;
}

.family-card:first-child{border-left:2px solid #888}

.family-photo{
grid-column:1;
grid-row:1 / span 5;
height:clamp(100px,16vh,140px);
width:100%;
max-width:125px;
margin:0;
padding:6px;
border:1px solid #555;
position:relative;
}

.family-photo img{
width:100%;
height:100%;
object-fit:cover;
filter:grayscale(20%);
}

.family-photo:before,.family-photo:after{
content:"";
position:absolute;
width:25px;
height:25px;
}

.family-photo:before{
top:-5px;
left:-5px;
border-top:2px solid #ddd;
border-left:2px solid #ddd;
}

.family-photo:after{
bottom:-5px;
right:-5px;
border-bottom:2px solid #ddd;
border-right:2px solid #ddd;
}

.family-number{
grid-column:2;
grid-row:1;
font-size:10px;
letter-spacing:2px;
color:#aaa;
margin-bottom:2px;
}

.family-card h2{
grid-column:2;
grid-row:2;
font-size:clamp(12px,1.25vw,16px);
letter-spacing:.5px;
color:#eee;
margin:0;
line-height:1.35;
overflow-wrap:anywhere;
}

.family-card .role{
grid-column:2;
grid-row:3;
color:#ddd;
font-size:10px;
letter-spacing:1px;
line-height:1.4;
margin:0;
}

.family-card p{
grid-column:2;
grid-row:4;
font-size:11px;
color:#bbb;
line-height:1.5;
margin:0;
}

.family-card .school{
grid-column:2;
grid-row:5;
margin:0;
color:#999;
font-size:10px;
}

.page4-footer{margin-top:8px;min-height:38px;flex-shrink:0}

/* RESPONSIVE */
@media(max-width:650px){
#page1,#page3{padding:14px 5%}
#page2{padding:12px 4%}
#page4{padding:10px 3%}
nav{height:43px;min-height:43px}
.logo{font-size:8px;letter-spacing:1px}
.nav-links{gap:7px}
.nav-links button{font-size:6px;letter-spacing:.3px}
.hero{flex-direction:column-reverse;justify-content:center;gap:10px;text-align:center}
.photo-area{width:105px;height:125px}
.hero h1{font-size:clamp(26px,7vw,38px);margin-bottom:8px}
.tag{font-size:8px;margin-bottom:8px}
.subtitle{font-size:11px;margin-bottom:8px}
.description{font-size:10px;line-height:1.45;margin:auto}
.student-info{margin-top:8px;font-size:9px;line-height:1.6;text-align:left;display:inline-block}
.next-area{margin-top:12px}
.page-btn{padding:8px 10px;font-size:7px}
.bottom{font-size:7px;min-height:35px}
.page2-content{gap:5px}
.page2-hero{padding:5px 0}
.page2-hero .subtitle{font-size:9px;letter-spacing:3px;margin-bottom:5px}
.page2-hero h1{font-size:clamp(19px,5vw,29px);margin-bottom:5px}
.page2-hero>p{font-size:10px}
.personal-details{font-size:7px;gap:5px 10px;margin-top:7px}
.page2-main{gap:10px 14px}
.page2-main section h2{font-size:11px;letter-spacing:1.5px;margin-bottom:6px;padding-bottom:4px}
.page2-main section p{font-size:9px;line-height:1.35}
.skills-list{margin:5px 0}
.education-list{gap:9px}
.education-item{padding-left:6px}
.education-item .year{font-size:8px;letter-spacing:1px}
.education-item h3{font-size:9px}
.education-item p{font-size:8px!important}
.page2-footer,.page3-footer,.page4-footer{font-size:7px;letter-spacing:1px;padding-top:6px}
.page3-heading{margin-bottom:13px}
.page3-heading h1{font-size:clamp(25px,7vw,38px)}
.page3-heading p{font-size:10px}
.achievement-list{grid-template-columns:1fr 1fr;gap:12px 15px}
.achievement-item{padding-left:8px}
.achievement-item .date{font-size:8px;letter-spacing:1px;margin-bottom:4px}
.achievement-item h2{font-size:10px;margin-bottom:4px}
.achievement-item p{font-size:9px;line-height:1.35}

/* FAMILY PAGE MOBILE */
.page4-heading{padding:5px 0 8px}
.page4-heading .tag{margin-bottom:5px}
.page4-heading h1{font-size:clamp(21px,6vw,30px)}
.page4-heading p{font-size:9px}
.family-grid{gap:8px;padding:2px 0}
.profile-pair{gap:6px}
.family-card{
display:flex;
flex-direction:column;
justify-content:center;
align-items:center;
text-align:center;
padding:5px 3px;
gap:0;
}
.family-photo{
height:clamp(65px,11vh,90px);
width:100%;
max-width:90px;
margin:0 auto 6px;
padding:4px;
}
.family-number{
font-size:8px;
letter-spacing:.5px;
margin-bottom:4px;
}
.family-card h2{
font-size:clamp(9px,2.7vw,12px);
line-height:1.25;
margin-bottom:4px;
overflow-wrap:anywhere;
}
.family-card .role{
font-size:8px;
letter-spacing:.4px;
line-height:1.25;
margin-bottom:4px;
}
.family-card p{
font-size:9px;
line-height:1.3;
}
.family-card .school{
font-size:8px;
margin-top:4px;
}
.page4-footer{margin-top:4px;min-height:32px}
.binary-heart{
grid-template-columns:repeat(31,9px);
grid-auto-rows:12px;
opacity:.06;
}
.binary-heart span{font-size:8px;color:#888}
}

@media(max-height:650px) and (min-width:651px){
#page1,#page2,#page3,#page4{padding-top:10px;padding-bottom:10px}
.photo-area{height:min(55vh,260px);width:205px}
.hero h1{font-size:42px}
.description{font-size:11px;line-height:1.6}
.page2-main{gap:10px 30px}
.page2-main section p{font-size:10px;line-height:1.4}
.page3-heading{margin-bottom:12px}
.achievement-list{gap:12px 25px}
.achievement-item p{font-size:10px;line-height:1.4}
.page4-heading{padding:5px 0 8px}
.family-grid{gap:6px}
.family-photo{height:95px}
.family-card{row-gap:3px;padding:5px 8px}
.family-card p{font-size:10px}
.family-card h2{font-size:12px}
}
</style>
</head>

<body>

<!-- PAGE 1: HOME -->
<div class="page active" id="page1">
<div class="binary-rain" id="binaryRain"></div>
<div class="page1-content">

<nav>
<div class="logo page-title">HOME<span>.</span></div>
<div class="nav-links">
<button onclick="showPage(1)">HOME</button>
<button onclick="showPage(2)">PERSONAL INFORMATION</button>
<button onclick="showPage(3)">ACHIEVEMENTS</button>
<button onclick="showPage(4)">FAMILY & FRIENDS</button>
</div>
</nav>

<main class="hero">
<div class="hero-text">
<div class="tag">WELCOME TO MY PORTFOLIO</div>
<h1>BROOKLANE<br><span>ARANCA.</span></h1>
<div class="subtitle">BSIT WEB TECHNOLOGY STUDENT</div>
<p class="description">
An undergraduate Information Technology student
with a passion for art, web development, and website
design. I enjoy exploring my creativity, learning
new things, and continuously improving my skills
in both art and technology.

I look forward to growing as a future IT professional
through creative and meaningful projects.
</p>
<div class="student-info">
<div>UNIVERSITY OF THE CORDILLERAS</div>
<div>BACHELOR OF SCIENCE IN INFORMATION TECHNOLOGY</div>
<div>CITCS 1A · WEB TECHNOLOGY</div>
</div>
<div class="next-area">
<button class="page-btn" onclick="showPage(2)">NEXT PAGE →</button>
</div>
</div>

<div class="photo-area">
<img src="https://lh3.googleusercontent.com/d/1jbiFy5_546Gmt6OxwIoTXaR7_fBW-DPy" alt="Brooklane Layaban Aranca">
</div>
</main>

<footer class="bottom">
<span>© 2026 BROOKLANE ARANCA</span>
<span>01001010 · 10100101 · 01011001</span>
</footer>
</div>
</div>

<!-- PAGE 2: PERSONAL INFORMATION -->
<div class="page" id="page2">
<div class="page2-content">

<nav>
<div class="logo page-title">PERSONAL INFORMATION<span>.</span></div>
<div class="nav-links">
<button onclick="showPage(1)">HOME</button>
<button onclick="showPage(2)">PERSONAL INFORMATION</button>
<button onclick="showPage(3)">ACHIEVEMENTS</button>
<button onclick="showPage(4)">FAMILY & FRIENDS</button>
</div>
</nav>

<div class="page2-hero">
<div class="subtitle">INFORMATION TECHNOLOGY STUDENT</div>
<h1>Brooklane Layaban Aranca</h1>
<p>First-Year BSIT Web Technology Student at the University of the Cordilleras.</p>
<div class="personal-details">
<span>BIRTHDAY: MAY 19, 2007</span>
<span>AGE: 19</span>
<span>LOCATION: GOLDFIELD, ITOGON, BENGUET</span>
<span>EMAIL: arancabrooklane07@gmail.com</span>
<span>STUDENT ID: 26-0078-692</span>
</div>
</div>

<main class="page2-main">
<section>
<h2>Personal Information</h2>
<p>
I am Brooklane Layaban Aranca, a first-year
Information Technology student at the University
of the Cordilleras, currently taking Web Technology.
I have a passion for creativity and enjoy exploring
different forms of art and digital media. My interests
include art making, designing, playing games, video
editing, photo editing, and photography. I enjoy
learning new things and expressing my creativity
through different projects. As an IT student, my goal
is to gain more knowledge and improve my skills in
Web Technology, especially in website design and
development. I look forward to developing my abilities
and creating meaningful digital projects in the future.
</p>
</section>

<section>
<h2>Technical Skills</h2>
<div class="skills-list">
<p>— Basic Python Coding</p>
<p>— Web Design</p>
</div>
<p>
I have basic knowledge of website design and
development, allowing me to create simple and
visually appealing website layouts. I am also
familiar with the fundamentals of Python programming,
including basic coding concepts and problem-solving.
As an Information Technology student, I am
continuously learning and improving my technical
skills to gain more experience in web development
and programming. I am eager to explore new tools
and technologies, strengthen my abilities, and
apply what I learn to future projects.
</p>
</section>

<section class="education">
<h2>Educational Background</h2>
<div class="education-list">
<div class="education-item">
<div class="year">2026 – PRESENT</div>
<h3>Bachelor of Science in Information Technology</h3>
<p>University of the Cordilleras</p>
<p>1st Year – Web Technology</p>
</div>
<div class="education-item">
<div class="year">2021 – 2026</div>
<h3>High School</h3>
<p>Baguio City High School</p>
</div>
<div class="education-item">
<div class="year">2012 – 2020</div>
<h3>Elementary Education</h3>
<p>STEP Learning Academy</p>
</div>
</div>
</section>
</main>

<footer class="page2-footer">
<span>MY PERSONAL PORTFOLIO | LEARN • CREATE • INNOVATE</span>
<div style="display:flex;gap:8px">
<button class="page-btn" onclick="showPage(1)">← PREVIOUS PAGE</button>
<button class="page-btn" onclick="showPage(3)">NEXT PAGE →</button>
</div>
</footer>
</div>
</div>

<!-- PAGE 3: ACHIEVEMENTS -->
<div class="page" id="page3">
<div class="binary-rain" id="binaryRain3"></div>
<div class="page3-content">

<nav>
<div class="logo page-title">ACHIEVEMENTS<span>.</span></div>
<div class="nav-links">
<button onclick="showPage(1)">HOME</button>
<button onclick="showPage(2)">PERSONAL INFORMATION</button>
<button onclick="showPage(3)">ACHIEVEMENTS</button>
<button onclick="showPage(4)">FAMILY & FRIENDS</button>
</div>
</nav>

<main class="page3-main">
<div class="page3-heading">
<div class="tag">MILESTONES & RECOGNITION</div>
<h1>MY <span>ACHIEVEMENTS.</span></h1>
<p>A collection of my academic, cultural, and extracurricular experiences.</p>
</div>

<div class="achievement-list">
<section class="achievement-item">
<div class="date">GRADE 7</div>
<h2>Honor Student</h2>
<p>Recognized as an Honor Student at Baguio City High School.</p>
</section>
<section class="achievement-item">
<div class="date">GRADE 8</div>
<h2>Honor Student</h2>
<p>Recognized as an Honor Student at Baguio City High School.</p>
</section>
<section class="achievement-item">
<div class="date">SEPTEMBER 2023 · GRADE 10</div>
<h2>Batang Pinoy</h2>
<p>Participated in Batang Pinoy as a Grade 10 student.</p>
</section>
<section class="achievement-item">
<div class="date">AUGUST 21, 2025</div>
<h2>UNESCO International Students</h2>
<p>Attended the UNESCO International Students event.</p>
</section>
<section class="achievement-item">
<div class="date">JANUARY 31, 2026</div>
<h2>Tam-Awan Silaw nan Lawag</h2>
<p>Exhibited artwork at Tam-Awan Silaw nan Lawag.</p>
</section>
</div>
</main>

<footer class="page3-footer">
<span>© 2026 BROOKLANE ARANCA</span>
<div style="display:flex;gap:8px">
<button class="page-btn" onclick="showPage(2)">← PREVIOUS PAGE</button>
<button class="page-btn" onclick="showPage(4)">NEXT PAGE →</button>
</div>
</footer>
</div>
</div>

<!-- PAGE 4: FAMILY AND FRIENDS -->
<div class="page" id="page4">

<div class="binary-heart" id="heart4"></div>

<div class="page4-content">
<nav>
<div class="logo page-title">FAMILY & FRIENDS<span>.</span></div>
<div class="nav-links">
<button onclick="showPage(1)">HOME</button>
<button onclick="showPage(2)">PERSONAL INFORMATION</button>
<button onclick="showPage(3)">ACHIEVEMENTS</button>
<button onclick="showPage(4)">FAMILY & FRIENDS</button>
</div>
</nav>

<header class="page4-heading">
<div class="tag">THE PEOPLE WHO MATTER</div>
<h1>FAMILY <span>& FRIENDS.</span></h1>
<p>A special part of my life and the people who inspire me.</p>
</header>

<main class="family-grid">

<div class="profile-pair">

<section class="family-card">
<div class="family-photo">
<img src="https://lh3.googleusercontent.com/d/1jbiFy5_546Gmt6OxwIoTXaR7_fBW-DPy" alt="Brooklane Layaban Aranca">
</div>
<div class="family-number">01 / MYSELF</div>
<h2>BROOKLANE LAYABAN ARANCA</h2>
<div class="role">INFORMATION TECHNOLOGY STUDENT</div>
<p>A student enrolled at the University of the Cordilleras.</p>
<p class="school">BSIT · WEB TECHNOLOGY</p>
</section>

<section class="family-card">
<div class="family-photo">
<img src="https://lh3.googleusercontent.com/d/1p8gIf4zdHPtPkaPWQ9dqzFUoBRdtBXFy" alt="Zhanaia Shane Lesoc">
</div>
<div class="family-number">02 / MY GIRLFRIEND</div>
<h2>ZHANAIA SHANE LESOC</h2>
<div class="role">INFORMATION TECHNOLOGY STUDENT</div>
<p>My girlfriend and a student at the University of the Cordilleras.</p>
<p class="school">BSIT · WEB TECHNOLOGY</p>
</section>

</div>

<div class="profile-pair">

<section class="family-card">
<div class="family-photo">
<img src="https://lh3.googleusercontent.com/d/1xFKxlS4vMql93ety-XJhlA3ZcpKbFK4c" alt="D Amangao Aranca">
</div>
<div class="family-number">03 / MY FATHER</div>
<h2>D----- AMANGAO ARANCA</h2>
<div class="role">PHILIPPINE NATIONAL POLICE</div>
<p>My father, who works as a Police Officer in the Philippine National Police (PNP).</p>
</section>

<section class="family-card">
<div class="family-photo">
<img src="https://lh3.googleusercontent.com/d/1GBxfepefmdG6H0gt4nLVUJ7nLFoRnTj6" alt="Jane Layaban Aranca">
</div>
<div class="family-number">04 / MY MOTHER</div>
<h2>JANE LAYABAN ARANCA</h2>
<div class="role">CAREGIVER</div>
<p>My mother, currently working as a caregiver in Haifa, Israel.</p>
</section>

</div>
</main>

<footer class="page4-footer">
<span>© 2026 BROOKLANE ARANCA</span>
<button class="page-btn" onclick="showPage(3)">← PREVIOUS PAGE</button>
</footer>
</div>
</div>

<script>
/* PAGE NAVIGATION */
function showPage(pageNumber){
document.querySelectorAll(".page").forEach(page=>{
page.classList.remove("active");
});

document.getElementById("page"+pageNumber).classList.add("active");

const pageNames={
1:"HOME",
2:"PERSONAL INFORMATION",
3:"ACHIEVEMENTS",
4:"FAMILY & FRIENDS"
};

document.querySelectorAll(".page-title").forEach(title=>{
title.innerHTML=pageNames[pageNumber]+"<span>.</span>";
});
}

/* BINARY RAIN */
function createBinary(id){
const container=document.getElementById(id);

for(let i=0;i<35;i++){
const span=document.createElement("span");
let digits="";

for(let j=0;j<20;j++){
digits+=Math.random()>.5?"1\n":"0\n";
}

span.textContent=digits;
span.style.left=Math.random()*100+"%";
span.style.top=Math.random()*100+"vh";
span.style.animationDelay=Math.random()*-12+"s";
container.appendChild(span);
}
}

/* BINARY HEART */
function createBinaryHeart(id){
const container=document.getElementById(id);
const rows=29;
const cols=41;
const cells=[];

for(let y=0;y<rows;y++){
for(let x=0;x<cols;x++){

const nx=((x-(cols-1)/2)/(cols/2))*1.5;
const ny=(((rows-1)/2-y)/(rows/2))*1.5;

const shape=Math.pow(nx*nx+ny*ny-1,3)
-nx*nx*ny*ny*ny;

if(shape<=0){
const digit=document.createElement("span");
digit.textContent=Math.random()>.5?"1":"0";
container.appendChild(digit);
cells.push(digit);
}
}
}

setInterval(()=>{
cells.forEach(digit=>{
if(Math.random()>.5){
digit.textContent=Math.random()>.5?"1":"0";
}
});
},500);
}

/* INITIALIZE BACKGROUNDS */
createBinary("binaryRain");
createBinary("binaryRain3");
createBinaryHeart("heart4");
</script>

</body>
</html>
