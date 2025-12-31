<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>🌸 Jharna Saxena 🌸</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            background: linear-gradient(135deg, #ffe6f2 0%, #ffd6e7 100%);
            font-family: 'Segoe UI', 'Arial Rounded MT Bold', 'Apple Color Emoji', sans-serif;
            color: #5a3d5c;
            min-height: 100vh;
            padding: 20px;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: rgba(255, 255, 255, 0.92);
            border-radius: 40px;
            padding: 40px;
            box-shadow: 0 20px 60px rgba(255, 105, 180, 0.15);
            border: 3px solid #ffccdd;
            position: relative;
            overflow: hidden;
        }
        .container::before {
            content: "🌸✨🌸✨🌸✨";
            position: absolute;
            top: -15px;
            left: -15px;
            font-size: 24px;
            color: #ff99cc;
            opacity: 0.2;
            z-index: 0;
        }
        .header {
            text-align: center;
            margin-bottom: 50px;
            position: relative;
            z-index: 1;
        }
        .main-title {
            font-size: 4.5rem;
            background: linear-gradient(45deg, #ff66a3, #ff99cc, #ff66a3);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 15px;
            text-shadow: 3px 3px 0px rgba(255, 182, 193, 0.3);
            font-weight: 900;
        }
        .subtitle {
            font-size: 1.8rem;
            color: #cc6699;
            margin-bottom: 30px;
            font-style: italic;
        }
        .tagline {
            font-size: 1.4rem;
            color: #ff66a3;
            background: rgba(255, 240, 245, 0.8);
            padding: 12px 30px;
            border-radius: 50px;
            display: inline-block;
            border: 2px solid #ffccdd;
        }
        .badge-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
            margin: 40px 0;
        }
        .badge {
            background: linear-gradient(135deg, #ff99cc, #ff66a3);
            color: white;
            padding: 12px 25px;
            border-radius: 50px;
            font-weight: bold;
            font-size: 1.1rem;
            display: flex;
            align-items: center;
            gap: 8px;
            box-shadow: 0 6px 15px rgba(255, 105, 180, 0.3);
            transition: all 0.3s ease;
            border: 2px solid white;
        }
        .badge:hover {
            transform: translateY(-8px) scale(1.05);
            box-shadow: 0 12px 25px rgba(255, 105, 180, 0.4);
        }
        .social-links {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin: 50px 0;
            flex-wrap: wrap;
        }
        .social-card {
            background: white;
            padding: 25px 40px;
            border-radius: 25px;
            text-decoration: none;
            color: #ff66a3;
            font-weight: bold;
            font-size: 1.2rem;
            display: flex;
            align-items: center;
            gap: 15px;
            transition: all 0.3s ease;
            border: 3px solid #ffccdd;
            box-shadow: 0 10px 20px rgba(255, 182, 193, 0.2);
            position: relative;
            overflow: hidden;
        }
        .social-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 5px;
            background: linear-gradient(90deg, #ff99cc, #ff66a3, #ff99cc);
        }
        .social-card:hover {
            transform: translateY(-10px) rotate(2deg);
            box-shadow: 0 20px 40px rgba(255, 105, 180, 0.3);
            background: linear-gradient(135deg, #fff0f5, #ffe6f2);
        }
        .social-icon {
            font-size: 2.2rem;
            transition: transform 0.3s ease;
        }
        .social-card:hover .social-icon {
            transform: scale(1.3) rotate(10deg);
        }
        .stats-section {
            background: linear-gradient(135deg, #fff0f5, #ffe6f2);
            padding: 40px;
            border-radius: 30px;
            margin: 60px 0;
            border: 3px solid #ffccdd;
            position: relative;
        }
        .stats-title {
            text-align: center;
            font-size: 2.5rem;
            color: #ff66a3;
            margin-bottom: 40px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 15px;
        }
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }
        .stat-card {
            background: white;    padding: 30px;
            border-radius: 25px;
            text-align: center;
            border: 2px solid #ffccdd;
            transition: all 0.3s ease;
            position: relative;
        }
        .stat-card:hover {
            transform: translateY(-15px);
            box-shadow: 0 15px 30px rgba(255, 182, 193, 0.3);
        }
        .stat-card::after {
            content: '🌸';
            position: absolute;
            bottom: -15px;
            right: -15px;
            font-size: 30px;
            opacity: 0.3;
        }
        .stat-number {
            font-size: 3.5rem;
            background: linear-gradient(45deg, #ff66a3, #ff99cc);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            font-weight: 900;
            margin-bottom: 10px;
        }
        .stat-label {
            color: #cc6699;
            font-size: 1.3rem;
            font-weight: bold;
        }
        .achievement-section {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin: 60px 0;
        }
        .achievement-card {
            background: white;
            padding: 35px;
            border-radius: 30px;
            border: 3px solid #ffccdd;
            position: relative;
            overflow: hidden;
            transition: all 0.3s ease;
        }
        .achievement-card:hover {
            transform: translateY(-12px);
            box-shadow: 0 20px 40px rgba(255, 182, 193, 0.3);
        }
        .achievement-card::before {
            content: '🌟';
            position: absolute;
            top: 15px;
            right: 15px;
            font-size: 40px;
            opacity: 0.2;
        }
        .achievement-icon {
            font-size: 3.5rem;
            margin-bottom: 20px;
            color: #ff99cc;
        }
        .achievement-title {
            color: #ff66a3;
            font-size: 1.8rem;
            margin-bottom: 15px;
            font-weight: bold;
        }
        .achievement-desc {
            color: #5a3d5c;
            line-height: 1.6;
        }
        .tech-stack {
            background: linear-gradient(135deg, #fff5f8, #ffeef3);
            padding: 50px;
            border-radius: 35px;
            margin: 60px 0;
            border: 3px dashed #ff99cc;
        }
        .tech-title {
            text-align: center;
            font-size: 2.8rem;
            color: #ff66a3;
            margin-bottom: 40px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 20px;
        }
        .tech-icons {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 25px;
        }
        .tech-icon {
            background: white;
            width: 80px;
            height: 80px;
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2.5rem;
            color: #ff66a3;
            transition: all 0.3s ease;
            border: 3px solid #ffccdd;
            box-shadow: 0 8px 15px rgba(255, 182, 193, 0.2);
        }
        .tech-icon:hover {
            transform: scale(1.2) rotate(15deg);
            background: linear-gradient(135deg, #ff99cc, #ff66a3);
            color: white;
            box-shadow: 0 15px 25px rgba(255, 105, 180, 0.4);
        }
        .journey-section {
            position: relative;
            padding: 50px 0;
            margin: 60px 0;
        }
        .journey-title {
            text-align: center;
            font-size: 3rem;
            color: #ff66a3;
            margin-bottom: 50px;
        }
        .journey-path {
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: relative;
            margin: 0 auto;
            max-width: 900px;
        }
        .journey-path::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 5%;
            right: 5%;
            height: 6px;
            background: linear-gradient(90deg, #ff99cc, #ff66a3, #ff99cc);
            z-index: 1;
            border-radius: 3px;
        }
        .journey-step {
            background: white;
            padding: 25px;
            border-radius: 25px;
            width: 200px;
            text-align: center;
            z-index: 2;
            border: 3px solid #ffccdd;
            box-shadow: 0 10px 20px rgba(255, 182, 193, 0.3);
            position: relative;
            transition: all 0.3s ease;
        }
        .journey-step:hover {
            transform: scale(1.1) rotate(-3deg);
            box-shadow: 0 20px 40px rgba(255, 105, 180, 0.4);
        }
        .step-icon {
            font-size: 2.5rem;
            margin-bottom: 15px;
            color: #ff66a3;
        }
        .step-title {
            color: #cc6699;
            font-weight: bold;
            font-size: 1.2rem;
            margin-bottom: 10px;
        }
        .footer {
            text-align: center;
            padding: 50px 0 20px;
            border-top: 3px dashed #ffccdd;
            margin-top: 60px;
        }
        .footer-text {
            color: #ff66a3;
            font-size: 1.3rem;
            margin-bottom: 20px;
        }
        .heart {
            color: #ff3366;
            animation: heartbeat 1.5s ease-in-out infinite;
        }
        @keyframes heartbeat {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.1); }
        }
        .floating {
            animation: float 6s ease-in-out infinite;
        }
        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }
        @media (max-width: 768px) {
            .main-title {
                font-size: 3rem;
            }
            .journey-path {
                flex-direction: column;
                gap: 40px;
            }
            .journey-path::before {
                display: none;
            }
            .social-card {
                width: 100%;
                justify-content: center;
            }
            .stats-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- HEADER SECTION -->
        <div class="header">
            <h1 class="main-title">🌸 Jharna Saxena 🌸</h1>
            <p class="subtitle">B.Tech CS-AI | BS Data Science | REYES UC Berkeley Mentee</p>
            <div class="tagline">✨ Making magic happen with code & research ✨</div>
            <div class="badge-container">
                <div class="badge">🎓 Dual Degree Student</div>
                <div class="badge">🔬 Research Enthusiast</div>
                <div class="badge">🐍 Python Developer</div>
                <div class="badge">💖 She/Her</div>
                <div class="badge">🌟 UC Berkeley</div>
            </div>
        </div>
        <!-- SOCIAL LINKS -->
        <div class="social-links">
            <a href="https://github.com/JharnaSaxena" target="_blank" class="social-card">
                <span class="social-icon">🐙</span>
                <span>GitHub Profile</span>
            </a>
            <a href="https://www.linkedin.com/in/jharna-saxena-502a6a2ba/" target="_blank" class="social-card">
                <span class="social-icon">💼</span>
                <span>LinkedIn Profile</span>
            </a>
            <a href="https://www.instagram.com/studywith.gremlin/?next=%2F&hl=en" target="_blank" class="social-card">
                <span class="social-icon">📸</span>
                <span>Instagram</span>
            </a>
        </div>
        <!-- STATS SECTION -->
        <div class="stats-section">
            <h2 class="stats-title">✨ My Journey in Numbers ✨</h2>
            <div class="stats-grid">
                <div class="stat-card">
                    <div class="stat-number">2024</div>
                    <div class="stat-label">Started University Journey</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">2</div>
                    <div class="stat-label">Dual Degrees Pursuing</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">2025</div>
                    <div class="stat-label">REYES UC Berkeley Mentee</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">∞</div>
                    <div class="stat-label">Dreams & Possibilities</div>
                </div>
            </div>
        </div>
        <!-- ACHIEVEMENTS -->
        <div class="achievement-section">
            <div class="achievement-card">
                <div class="achievement-icon">🎓</div>
                <h3 class="achievement-title">UC Berkeley Research</h3>
                <p class="achievement-desc">Selected as REYES 2025 mentee under Dr. Naveed Jeelani Khan for bias research in e-commerce systems.</p>
            </div>
            <div class="achievement-card">
                <div class="achievement-icon">💻</div>
                <h3 class="achievement-title">Python4Physics</h3>
                <p class="achievement-desc">Completed intensive Python programming for physics at UC Berkeley with multiple projects.</p>
            </div>
            <div class="achievement-card">
                <div class="achievement-icon">📚</div>
                <h3 class="achievement-title">Dual Degrees</h3>
                <p class="achievement-desc">Pursuing B.Tech in Computer Science (AI) and BS in Data Science simultaneously.</p>
            </div>
        </div>
        <!-- TECH STACK -->
        <div class="tech-stack">
            <h2 class="tech-title">💻 Tech Stack & Skills</h2>
            <div class="tech-icons">
                <div class="tech-icon">🐍</div>
                <div class="tech-icon">📊</div>
                <div class="tech-icon">🤖</div>
                <div class="tech-icon">🔍</div>
                <div class="tech-icon">📈</div>
                <div class="tech-icon">💾</div>
                <div class="tech-icon">📚</div>
                <div class="tech-icon">🎯</div>
            </div>
        </div>
        <!-- JOURNEY TIMELINE -->
        <div class="journey-section">
            <h2 class="journey-title">🦋 My Magical Journey</h2>
            <div class="journey-path">
                <div class="journey-step floating">
                    <div class="step-icon">🎓</div>
                    <div class="step-title">Freshman Year</div>
                    <p>Started CS journey with passion</p>
                </div>
                <div class="journey-step floating" style="animation-delay: 1s;">
                    <div class="step-icon">🌟</div>
                    <div class="step-title">REYES Selection</div>
                    <p>Got into UC Berkeley program</p>
                </div>
                <div class="journey-step floating" style="animation-delay: 2s;">
                    <div class="step-icon">🔬</div>
                    <div class="step-title">Research Mentee</div>
                    <p>Working on e-commerce bias</p>
                </div>
            </div>
        </div>
        <!-- FOOTER -->
        <div class="footer">
            <p class="footer-text">
                Made with <span class="heart">💖</span> by Jharna Saxena
            </p>
            <p class="footer-text">
                ✨ Every day is a new opportunity to learn and grow ✨
            </p>
            <p class="footer-text">
                <em>"From skipping Day 1 for Harry Potter to finishing strong at Berkeley!"</em>
            </p>
        </div>
    </div>
    <script>
        // Add floating animation to achievement cards
        document.querySelectorAll('.achievement-card').forEach((card, index) => {
            card.style.animationDelay = `${index * 0.3}s`;
            card.classList.add('floating');
        });
        // Add hover effect to journey steps
        document.querySelectorAll('.journey-step').forEach(step => {
            step.addEventListener('mouseenter', () => {
                step.style.transform = 'scale(1.1) rotate(-3deg)';
            });
            step.addEventListener('mouseleave', () => {
                step.style.transform = 'scale(1) rotate(0deg)';
            });
        });
        const sparkles = ['✨', '🌸', '🌟', '💫', '🎀', '🦋', '💖'];
        const container = document.querySelector('.container');
        function createSparkle() {
            const sparkle = document.createElement('div');
            sparkle.textContent = sparkles[Math.floor(Math.random() * sparkles.length)];
            sparkle.style.position = 'absolute';
            sparkle.style.left = Math.random() * 100 + '%';
            sparkle.style.top = Math.random() * 100 + '%';
            sparkle.style.opacity = '0.1';
            sparkle.style.fontSize = (Math.random() * 30 + 20) + 'px';
            sparkle.style.zIndex = '0';
            sparkle.style.pointerEvents = 'none';
            sparkle.style.animation = `float ${Math.random() * 4 + 3}s ease-in-out infinite`;
            sparkle.style.animationDelay = Math.random() * 2 + 's';
            container.appendChild(sparkle);
            setTimeout(() => {
                if (sparkle.parentNode === container) {
                    container.removeChild(sparkle);
                }
            }, 10000);
        }
        for (let i = 0; i < 20; i++) {
            setTimeout(() => createSparkle(), i * 300);
        }
        setInterval(() => {
            if (document.hasFocus()) {
                createSparkle();
            }
        }, 2000);
    </script>
</body>
</html>
