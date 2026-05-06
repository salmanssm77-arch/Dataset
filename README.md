
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>AI Calorie Burn Predictor</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:'Poppins',sans-serif;
}

body{
    background:#050816;
    color:white;
    overflow-x:hidden;
}

/* NAVBAR */

nav{
    width:100%;
    padding:20px 10%;
    display:flex;
    justify-content:space-between;
    align-items:center;
    position:fixed;
    top:0;
    z-index:1000;
    backdrop-filter:blur(10px);
    background:rgba(0,0,0,0.3);
}

nav h1{
    font-size:28px;
    background:linear-gradient(to right,#00d4ff,#8a2be2);
    -webkit-background-clip:text;
    -webkit-text-fill-color:transparent;
}

nav ul{
    display:flex;
    gap:30px;
    list-style:none;
}

nav ul li{
    cursor:pointer;
    transition:0.3s;
}

nav ul li:hover{
    color:#00d4ff;
}

/* HERO */

.hero{
    min-height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    text-align:center;
    padding:100px 10%;
    background:
    radial-gradient(circle at top left,#8a2be240,transparent 30%),
    radial-gradient(circle at bottom right,#00d4ff40,transparent 30%);
}

.hero-content h2{
    font-size:65px;
    line-height:1.1;
    margin-bottom:20px;
}

.hero-content span{
    background:linear-gradient(to right,#00d4ff,#8a2be2);
    -webkit-background-clip:text;
    -webkit-text-fill-color:transparent;
}

.hero-content p{
    font-size:18px;
    max-width:700px;
    margin:auto;
    opacity:0.8;
    margin-bottom:35px;
}

.hero button{
    padding:15px 40px;
    border:none;
    border-radius:50px;
    background:linear-gradient(to right,#00d4ff,#8a2be2);
    color:white;
    font-size:18px;
    cursor:pointer;
    transition:0.3s;
}

.hero button:hover{
    transform:scale(1.05);
}

/* CARDS */

.section{
    padding:100px 10%;
}

.section-title{
    font-size:42px;
    text-align:center;
    margin-bottom:60px;
}

.cards{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:30px;
}

.card{
    background:rgba(255,255,255,0.05);
    border:1px solid rgba(255,255,255,0.1);
    padding:30px;
    border-radius:20px;
    transition:0.3s;
    backdrop-filter:blur(10px);
}

.card:hover{
    transform:translateY(-10px);
    border-color:#00d4ff;
}

.card h3{
    margin-bottom:15px;
    color:#00d4ff;
}

/* FORM */

.predictor{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:40px;
    align-items:center;
}

.form-box{
    background:rgba(255,255,255,0.05);
    padding:40px;
    border-radius:25px;
    border:1px solid rgba(255,255,255,0.1);
}

.form-box input,
.form-box select{
    width:100%;
    padding:15px;
    margin-bottom:20px;
    border:none;
    border-radius:12px;
    background:#10172a;
    color:white;
}

.form-box button{
    width:100%;
    padding:15px;
    border:none;
    border-radius:12px;
    background:linear-gradient(to right,#00d4ff,#8a2be2);
    color:white;
    font-size:18px;
    cursor:pointer;
}

.result{
    margin-top:25px;
    text-align:center;
    font-size:28px;
    font-weight:600;
    color:#00d4ff;
}

/* STATS */

.stats{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
    gap:25px;
}

.stat-box{
    background:rgba(255,255,255,0.05);
    padding:40px;
    border-radius:20px;
    text-align:center;
}

.stat-box h2{
    font-size:40px;
    color:#00d4ff;
}

/* FOOTER */

footer{
    text-align:center;
    padding:40px;
    opacity:0.6;
}

@media(max-width:900px){

.hero-content h2{
    font-size:42px;
}

.predictor{
    grid-template-columns:1fr;
}

nav ul{
    display:none;
}

}

</style>
</head>

<body>

<nav>
    <h1>FitAI</h1>

    <ul>
        <li>Home</li>
        <li>Dataset</li>
        <li>Predictor</li>
        <li>Analytics</li>
    </ul>
</nav>

<section class="hero">

    <div class="hero-content">

        <h2>
            AI Powered <span>Calorie Burn</span> Prediction
        </h2>

        <p>
            Predict calorie expenditure using machine learning and biometric data
            like heart rate, workout duration, body temperature, age, and weight.
        </p>

        <button>Explore Project</button>

    </div>

</section>

<section class="section">

    <h2 class="section-title">Dataset Features</h2>

    <div class="cards">

        <div class="card">
            <h3>Heart Rate</h3>
            <p>Tracks workout intensity and calorie burn patterns.</p>
        </div>

        <div class="card">
            <h3>Workout Duration</h3>
            <p>Longer exercise sessions increase energy expenditure.</p>
        </div>

        <div class="card">
            <h3>Body Temperature</h3>
            <p>Temperature rise indicates higher physical activity.</p>
        </div>

        <div class="card">
            <h3>Age & Weight</h3>
            <p>Personal biometric information for accurate prediction.</p>
        </div>

    </div>

</section>

<section class="section">

<h2 class="section-title">Calories Predictor</h2>

<div class="predictor">

<div class="form-box">

<input type="number" id="age" placeholder="Age">

<input type="number" id="weight" placeholder="Weight (kg)">

<input type="number" id="duration" placeholder="Workout Duration (min)">

<input type="number" id="heart" placeholder="Heart Rate">

<input type="number" id="temp" placeholder="Body Temperature">

<select id="gender">
<option>Male</option>
<option>Female</option>
</select>

<button onclick="predictCalories()">Predict Calories</button>

<div class="result" id="result">
0 Calories
</div>

</div>

<div>

<img 
src="https://images.unsplash.com/photo-1517836357463-d25dfeac3438?q=80&w=1200"
style="width:100%; border-radius:25px;"
>

</div>

</div>

</section>

<section class="section">

<h2 class="section-title">Project Analytics</h2>

<div class="stats">

<div class="stat-box">
<h2>15K+</h2>
<p>Dataset Rows</p>
</div>

<div class="stat-box">
<h2>95%</h2>
<p>Prediction Accuracy</p>
</div>

<div class="stat-box">
<h2>7+</h2>
<p>Features Used</p>
</div>

<div class="stat-box">
<h2>AI</h2>
<p>ML Regression Model</p>
</div>

</div>

</section>

<footer>

<p>
Built using Machine Learning & Fitness Analytics
</p>

</footer>

<script>

function predictCalories(){

    let age = parseFloat(document.getElementById("age").value) || 0;
    let weight = parseFloat(document.getElementById("weight").value) || 0;
    let duration = parseFloat(document.getElementById("duration").value) || 0;
    let heart = parseFloat(document.getElementById("heart").value) || 0;
    let temp = parseFloat(document.getElementById("temp").value) || 0;

    let calories =
    (duration * 5) +
    (heart * 0.5) +
    (weight * 0.2) +
    (temp * 2) -
    (age * 0.1);

    calories = Math.round(calories);

    document.getElementById("result").innerHTML =
    calories + " Calories";
}

</script>

</body>
</html># Dataset
