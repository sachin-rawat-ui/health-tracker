<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>NutriIndia Pro X Fitness+</title>
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<style>
/* PART 2 CSS WILL COME HERE */
</style>
</head>
<body>

<!-- NAVBAR -->
<header class="navbar">
    <div class="logo">💪 NutriIndia Pro X</div>
    <nav>
        <button class="nav-btn active" onclick="showPage('dashboard')">Dashboard</button>
        <button class="nav-btn" onclick="showPage('fitness')">Fitness Gallery</button>
        <button class="nav-btn" onclick="showPage('water')">Water Tracker</button>
        <button class="nav-btn" onclick="showPage('analytics')">Analytics</button>
    </nav>
</header>

<!-- DASHBOARD PAGE -->
<section id="dashboard" class="page active-page">
    <div class="hero-card">
        <h1>Nutrition & Fitness Tracker</h1>
        <p>Track calories, water, body goals, and fitness progress in one premium dashboard.</p>
    </div>

    <div class="stats-grid">
        <div class="stat-card">
            <h3>Total Calories</h3>
            <p id="totalCalories">0</p>
        </div>
        <div class="stat-card">
            <h3>Protein</h3>
            <p id="totalProtein">0g</p>
        </div>
        <div class="stat-card">
            <h3>Carbs</h3>
            <p id="totalCarbs">0g</p>
        </div>
        <div class="stat-card">
            <h3>Fats</h3>
            <p id="totalFats">0g</p>
        </div>
    </div>

    <div class="tracker-box">
        <h2>Food Search</h2>
        <input type="text" id="foodSearch" placeholder="Search Indian foods...">
        <div id="foodResults"></div>
    </div>

    <div class="tracker-box">
        <h2>Workout Suggestions</h2>
        <select id="goalSelector">
            <option value="fatloss">Fat Loss</option>
            <option value="musclegain">Muscle Gain</option>
            <option value="weightgain">Weight Gain</option>
        </select>
        <button onclick="generateWorkout()">Generate Workout</button>
        <div id="workoutPlan"></div>
    </div>

    <div class="tracker-box">
        <h2>Motivation</h2>
        <p id="motivationQuote">Push yourself, because no one else is going to do it for you.</p>
        <button onclick="newQuote()">New Quote</button>
    </div>
</section>

<!-- FITNESS GALLERY PAGE -->
<section id="fitness" class="page">
    <h2>Fitness Inspiration Gallery</h2>

    <div class="gallery-grid">

        <div class="fitness-card">
            <img src="https://images.unsplash.com/photo-1571019613454-1cb2f99b2d8b" alt="">
            <h3>Fat Loss Physique</h3>
            <p>Lean shredded transformation inspiration.</p>
        </div>

        <div class="fitness-card">
            <img src="https://images.unsplash.com/photo-1517836357463-d25dfeac3438" alt="">
            <h3>Muscle Gain</h3>
            <p>Build dense muscular frame.</p>
        </div>

        <div class="fitness-card">
            <img src="https://images.unsplash.com/photo-1534438327276-14e5300c3a48" alt="">
            <h3>Weight Gain Bulk</h3>
            <p>Healthy bulking transformation goal.</p>
        </div>

        <div class="fitness-card">
            <img src="https://images.unsplash.com/photo-1518611012118-696072aa579a" alt="">
            <h3>Fitness Athlete</h3>
            <p>Elite conditioning motivation.</p>
        </div>

    </div>
</section>

<!-- WATER TRACKER PAGE -->
<section id="water" class="page">
    <h2>Daily Water Tracker</h2>

    <div class="water-box">
        <div class="water-progress">
            <div id="waterFill"></div>
        </div>

        <h3><span id="waterAmount">0</span> / 3000 ml</h3>

        <div class="water-buttons">
            <button onclick="addWater(250)">+250ml</button>
            <button onclick="addWater(500)">+500ml</button>
            <button onclick="resetWater()">Reset</button>
        </div>
    </div>
</section>

<!-- ANALYTICS PAGE -->
<section id="analytics" class="page">
    <h2>Progress Analytics</h2>

    <div class="chart-grid">
        <div class="chart-card">
            <h3>Calories vs Goal</h3>
            <canvas id="calorieChart"></canvas>
        </div>

        <div class="chart-card">
            <h3>Macro Split</h3>
            <canvas id="macroChart"></canvas>
        </div>

        <div class="chart-card">
            <h3>Weekly Trend</h3>
            <canvas id="weeklyChart"></canvas>
        </div>
    </div>
</section>

<script>
/* PART 3 JS WILL COME HERE */
</script>

</body>
</html>
