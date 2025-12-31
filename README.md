<!DOCTYPE html>
<html>
<head>
    <style>
        /* === BABY PINK BACKGROUND & GLOBAL STYLES === */
        body {
            background-color: #ffe6f2 !important;
            background-image: 
                radial-gradient(#ffccdd 15%, transparent 16%),
                radial-gradient(#ffccdd 15%, transparent 16%);
            background-size: 60px 60px;
            background-position: 0 0, 30px 30px;
            font-family: 'Segoe UI', 'Arial Rounded MT Bold', 'Helvetica Neue', sans-serif;
            color: #5a3d5c;
            margin: 0;
            padding: 20px;
            line-height: 1.6;
        }
        
        /* === CONTAINER WITH SOFT EDGES === */
        .container {
            max-width: 900px;
            margin: 0 auto;
            background-color: rgba(255, 255, 255, 0.85);
            border-radius: 30px;
            padding: 40px;
            box-shadow: 0 15px 35px rgba(255, 182, 193, 0.3);
            border: 2px solid #ffccdd;
            position: relative;
            overflow: hidden;
        }
        
        /* === DECORATIVE ELEMENTS === */
        .container::before {
            content: "🌸✨🌸✨";
            position: absolute;
            top: 10px;
            left: 10px;
            font-size: 20px;
            color: #ff99bb;
            opacity: 0.3;
        }
        
        .container::after {
            content: "✨🌸✨🌸";
            position: absolute;
            bottom: 10px;
            right: 10px;
            font-size: 20px;
            color: #ff99bb;
            opacity: 0.3;
        }
        
        /* === HEADER SECTION === */
        .header {
            text-align: center;
            margin-bottom: 40px;
            padding-bottom: 30px;
            border-bottom: 3px dashed #ff99bb;
            position: relative;
        }
        
        .name-title {
            font-size: 3.5em;
            background: linear-gradient(45deg, #ff66a3, #ff99cc, #ff66a3);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 10px;
            text-shadow: 3px 3px 0px rgba(255, 182, 193, 0.2);
            font-weight: 800;
        }
        
        .tagline {
            font-size: 1.3em;
            color: #cc6699;
            margin-top: 0;
            font-style: italic;
        }
        
        /* === BADGES SECTION === */
        .badges {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 10px;
            margin: 30px 0;
        }
        
        .badge {
            background: linear-gradient(45deg, #ffb6c1, #ff99cc);
            color: white;
            padding: 8px 18px;
            border-radius: 50px;
            font-size: 0.9em;
            font-weight: bold;
            display: inline-block;
            box-shadow: 0 4px 10px rgba(255, 105, 180, 0.3);
            transition: all 0.3s ease;
            border: 2px solid white;
        }
        
        .badge:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 15px rgba(255, 105, 180, 0.4);
        }
        
        /* === STATS SECTION === */
        .stats-section {
            text-align: center;
            margin: 40px 0;
            padding: 25px;
            background: rgba(255, 240, 245, 0.7);
            border-radius: 20px;
            border: 2px solid #ffccdd;
        }
        
        .stats-title {
            color: #ff66a3;
            font-size: 1.8em;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
        }
        
        /* === SECTIONS COMMON STYLES === */
        .section {
            margin: 50px 0;
            padding: 30px;
            background: rgba(255, 255, 255, 0.7);
            border-radius: 25px;
            border-left: 10px solid #ff99cc;
            box-shadow: 0 8px 20px rgba(255, 182, 193, 0.2);
            position: relative;
        }
        
        .section-title {
            color: #ff66a3;
            font-size: 2.2em;
            margin-top: 0;
            margin-bottom: 25px;
            padding-bottom: 15px;
            border-bottom: 2px solid #ffccdd;
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .section-title::before {
            font-size: 1.5em;
        }
        
        /* === ABOUT ME SECTION === */
        .about-box {
            display: flex;
            align-items: center;
            gap: 30px;
            flex-wrap: wrap;
        }
        
        .about-text {
            flex: 1;
            min-width: 300px;
        }
        
        .yaml-box {
            background: #fff0f5;
            padding: 25px;
            border-radius: 20px;
            border: 2px dashed #ff99cc;
            font-family: 'Courier New', monospace;
            color: #cc6699;
            flex: 1;
            min-width: 300px;
        }
        
        /* === JOURNEY TIMELINE === */
        .timeline {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            margin: 40px 0;
            position: relative;
        }
        
        .timeline::before {
            content: "";
            position: absolute;
            top: 50%;
            left: 5%;
            right: 5%;
            height: 4px;
            background: linear-gradient(90deg, #ff99cc, #ff66a3, #ff99cc);
            z-index: 1;
        }
        
        .timeline-item {
            background: white;
            border-radius: 20px;
            padding: 20px;
            width: 220px;
            text-align: center;
            z-index: 2;
            margin: 10px;
            border: 3px solid #ffccdd;
            box-shadow: 0 10px 20px rgba(255, 182, 193, 0.3);
            transition: transform 0.3s ease;
        }
        
        .timeline-item:hover {
            transform: scale(1.05);
        }
        
        .timeline-date {
            font-weight: bold;
            color: #ff66a3;
            font-size: 1.2em;
            margin-bottom: 10px;
        }
        
        /* === PROJECTS TABLE === */
        .projects-table {
            width: 100%;
            border-collapse: separate;
            border-spacing: 0 15px;
            margin: 30px 0;
        }
        
        .projects-table th {
            background: linear-gradient(45deg, #ff99cc, #ff66a3);
            color: white;
            padding: 15px;
            text-align: left;
            border-radius: 15px 15px 0 0;
            font-size: 1.2em;
        }
        
        .projects-table td {
            background: #fff5f8;
            padding: 20px;
            border-radius: 15px;
            border: 2px solid #ffccdd;
        }
        
        .project-link {
            background: #ff99cc;
            color: white;
            padding: 8px 15px;
            border-radius: 20px;
            text-decoration: none;
            display: inline-block;
            transition: all 0.3s ease;
        }
        
        .project-link:hover {
            background: #ff66a3;
            transform: translateX(5px);
        }
        
        /* === RESEARCH HIGHLIGHT === */
        .research-highlight {
            background: linear-gradient(135deg, #fff0f5, #ffe6f2);
            padding: 35px;
            border-radius: 25px;
            border: 3px solid #ff99cc;
            margin: 40px 0;
            position: relative;
            overflow: hidden;
        }
        
        .research-highlight::before {
            content: "🌟";
            position: absolute;
            top: -15px;
            right: -15px;
            font-size: 100px;
            opacity: 0.1;
            transform: rotate(15deg);
        }
        
        /* === SKILLS BOX === */
        .skills-box {
            background: #fff0f5;
            padding: 30px;
            border-radius: 20px;
            border: 3px solid #ffccdd;
            font-family: 'Courier New', monospace;
            font-size: 1.1em;
            line-height: 1.8;
            color: #cc6699;
            margin: 30px 0;
        }
        
        /* === FUN FACTS === */
        .fun-facts {
            display: flex;
            align-items: center;
            gap: 30px;
            flex-wrap: wrap;
        }
        
        .facts-list {
            flex: 1;
            min-width: 300px;
            background: #fff5f8;
            padding: 25px;
            border-radius: 20px;
            border: 2px solid #ffccdd;
        }
        
        .facts-list li {
            margin: 15px 0;
            padding-left: 30px;
            position: relative;
        }
        
        .facts-list li::before {
            content: "✨";
            position: absolute;
            left: 0;
            color: #ff66a3;
        }
        
        /* === CONNECT SECTION === */
        .connect-buttons {
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
            margin: 40px 0;
        }
        
        .connect-button {
            background: linear-gradient(45deg, #ff66a3, #ff99cc);
            color: white;
            padding: 15px 35px;
            border-radius: 50px;
            text-decoration: none;
            font-size: 1.2em;
            font-weight: bold;
            display: flex;
            align-items: center;
            gap: 10px;
            box-shadow: 0 8px 20px rgba(255, 105, 180, 0.4);
            transition: all 0.3s ease;
            border: 3px solid white;
        }
        
        .connect-button:hover {
            transform: translateY(-8px) scale(1.05);
            box-shadow: 0 15px 30px rgba(255, 105, 180, 0.6);
        }
        
        /* === QUOTE SECTION === */
        .quote-box {
            background: linear-gradient(135deg, #ffccdd, #ffb6c1);
            color: white;
            padding: 40px;
            border-radius: 25px;
            text-align: center;
            margin: 50px 0;
            position: relative;
            overflow: hidden;
        }
        
        .quote-box::before {
            content: "❝";
            position: absolute;
            top: -20px;
            left: 20px;
            font-size: 100px;
            opacity: 0.3;
        }
        
        .quote-box::after {
            content: "❞";
            position: absolute;
            bottom: -40px;
            right: 20px;
            font-size: 100px;
            opacity: 0.3;
        }
        
        .quote-text {
            font-size: 1.5em;
            font-style: italic;
            margin: 0;
            position: relative;
            z-index: 2;
        }
        
        /* === FOOTER === */
        .footer {
            text-align: center;
            margin-top: 60px;
            padding-top: 30px;
            border-top: 3px dashed #ff99bb;
            color: #cc6699;
        }
        
        /* === RESPONSIVE DESIGN === */
        @media (max-width: 768px) {
            .container {
                padding: 20px;
                border-radius: 20px;
            }
            
            .name-title {
                font-size: 2.5em;
            }
            
            .timeline {
                flex-direction: column;
            }
            
            .timeline::before {
                display: none;
            }
            
            .connect-buttons {
                flex-direction: column;
                align-items: center;
            }
        }
        
        /* === ANIMATIONS === */
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0px); }
        }
        
        .floating {
            animation: float 5s ease-in-out infinite;
        }
        
        .highlight {
            background: linear-gradient(120deg, #ff99cc 0%, #ff99cc 100%);
            background-repeat: no-repeat;
            background-size: 100% 0.4em;
            background-position: 0 90%;
            transition: background-size 0.25s ease-in;
        }
        
        .highlight:hover {
            background-size: 100% 100%;
            color: white;
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- HEADER -->
        <div class="header">
            <h1 class="name-title">🌸 Jharna Saxena 🌸</h1>
            <p class="tagline">CS-AI & Data Science Student | REYES UC Berkeley Mentee | Passionate Researcher</p>
            
            <div class="badges">
                <span class="badge">✨ Dreamer & Doer</span>
                <span class="badge">🎓 CS-AI & Data Science</span>
                <span class="badge">🌟 REYES UC Berkeley</span>
                <span class="badge">👩‍💻 Python Developer</span>
                <span class="badge">🔬 Research Enthusiast</span>
            </div>
        </div>
        
        <!-- ABOUT ME -->
        <div class="section">
            <h2 class="section-title">🎀 About Me</h2>
            <div class="about-box">
                <div class="about-text">
                    <p>Hi there! I'm Jharna 🌸 A passionate Computer Science and Data Science student who believes in adding a touch of softness to everything—even code!</p>
                    <p><strong>Pronouns:</strong> She/Her</p>
                    <p><strong>Fun Fact:</strong> I'm weak in math but still pursuing Data Science! (Yes, really! 🎀)</p>
                    <p>From skipping Day 1 for Harry Potter to completing Python4Physics at UC Berkeley, I've learned that <span class="highlight">persistence beats perfection every time</span>!</p>
                </div>
                <div class="yaml-box">
                    <pre>
name: Jharna Saxena
pronouns: She/Her
current_roles:
  - B.Tech in Computer Science (AI)
  - BS in Data Science
  - REYES 2025 Mentee @ UC Berkeley
personality:
  - 💖 Soft-hearted but resilient
  - 🌸 Loves pastel aesthetics
  - ✨ Believes in magic of hard work
motto: "Fiat Lux ✨"</pre>
                </div>
            </div>
        </div>
        
        <!-- MY JOURNEY -->
        <div class="section">
            <h2 class="section-title">🦋 My Magical Journey</h2>
            <div class="timeline">
                <div class="timeline-item floating">
                    <div class="timeline-date">Feb 2025</div>
                    <div>🎓 Freshman with SGPA: 7.0</div>
                    <div>Almost didn't apply for REYES</div>
                </div>
                
                <div class="timeline-item floating" style="animation-delay: 0.5s;">
                    <div class="timeline-date">Jun 2025</div>
                    <div>🌟 REYES General Program</div>
                    <div>Skipped Day 1 for Harry Potter! 🪄</div>
                </div>
                
                <div class="timeline-item floating" style="animation-delay: 1s;">
                    <div class="timeline-date">Jul 2025</div>
                    <div>🔬 Research Mentee @ UC Berkeley</div>
                    <div>Working on bias in e-commerce</div>
                </div>
                
                <div class="timeline-item floating" style="animation-delay: 1.5s;">
                    <div class="timeline-date">Present</div>
                    <div>✨ Still learning & growing</div>
                    <div>Making magic happen every day</div>
                </div>
            </div>
        </div>
        
        <!-- PROJECTS -->
        <div class="section">
            <h2 class="section-title">🌌 Python4Physics Projects</h2>
            <table class="projects-table">
                <thead>
                    <tr>
                        <th>Project</th>
                        <th>Description</th>
                        <th>Link</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td><strong>📊 Project 1</strong></td>
                        <td>Basic Python Exercises</td>
                        <td><a href="https://lnkd.in/dezf4WGp" class="project-link">View →</a></td>
                    </tr>
                    <tr>
                        <td><strong>⚡ Project 2</strong></td>
                        <td>Foundations of Programming</td>
                        <td><a href="https://lnkd.in/dsmxn4Kw" class="project-link">View →</a></td>
                    </tr>
                    <tr>
                        <td><strong>🌟 Project 3</strong></td>
                        <td>Radi Analysis</td>
                        <td><a href="https://lnkd.in/dn_DXneV" class="project-link">View →</a></td>
                    </tr>
                    <tr>
                        <td><strong>📈 Project 4</strong></td>
                        <td>Body Decay Simulation</td>
                        <td><a href="https://lnkd.in/dUczR_3R" class="project-link">View →</a></td>
                    </tr>
                </tbody>
            </table>
        </div>
        
        <!-- RESEARCH HIGHLIGHT -->
        <div class="research-highlight">
            <h2 style="color: #ff66a3; margin-top: 0;">🌸 Research Journey @ UC Berkeley</h2>
            <p><strong>Project:</strong> "Exploring bias and its effects in online e-commerce platform review systems"</p>
            <p><strong>Mentor:</strong> Dr. Naveed Jeelani Khan, Ph.D (REYES, UC Berkeley)</p>
            <p><strong>My Experience:</strong></p>
            <ul style="color: #5a3d5c;">
                <li>📝 Independently drafted literature review when meetings slowed down</li>
                <li>💌 Sent 7 polite follow-up emails (patience is key!)</li>
                <li>🎓 Earned my certificate in December 2025 after persistent effort</li>
                <li>🦋 Learned that <strong>showing up matters more than being perfect</strong></li>
            </ul>
            <p style="font-style: italic; color: #cc6699; margin-top: 20px;">
                "Sometimes the only qualification you need is the courage to apply."
            </p>
        </div>
        
        <!-- SKILLS -->
        <div class="section">
            <h2 class="section-title">🍓 Skills & Tech Stack</h2>
            <div class="skills-box">
                <pre>
# My Tech Toolkit
Languages     = ["Python", "SQL"]
Data Science  = ["Pandas", "NumPy", "Statistics", "Experimental Design"]
Research      = ["Literature Review", "Critical Analysis", "Academic Writing"]
Soft Skills   = ["Persistence", "Communication", "Independent Learning"]
Currently     = ["Machine Learning", "Advanced Python", "Research Methods"]

# Secret Ingredients
ingredient_1 = "🌸 Believing in myself even when math feels scary"
ingredient_2 = "✨ Courage to apply even when feeling underqualified"
ingredient_3 = "🎀 Adding softness to everything I do"</pre>
            </div>
        </div>
        
        <!-- FUN FACTS -->
        <div class="section">
            <h2 class="section-title">🎪 Fun Facts & Quirks</h2>
            <div class="fun-facts">
                <div class="facts-list">
                    <ul>
                        <li>I'm weak in math but still pursuing Data Science (yes, really!)</li>
                        <li>Skipped Day 1 of Python4Physics for Harry Potter and still completed everything</li>
                        <li>Love all things soft, pastel, and magical ✨</li>
                        <li>Sent 7 follow-up emails to get my research certificate (patience is key!)</li>
                        <li>Believe in adding a touch of softness to everything, even code</li>
                    </ul>
                </div>
                <div style="flex: 1; text-align: center; min-width: 300px;">
                    <div style="font-size: 100px; color: #ff99cc;">🎀</div>
                    <p><em>"From hesitant freshman to Berkeley mentee - magic happens outside your comfort zone!"</em></p>
                </div>
            </div>
        </div>
        
        <!-- CONNECT -->
        <div class="section">
            <h2 class="section-title">💌 Let's Connect!</h2>
            <div class="connect-buttons">
                <a href="mailto:j9610577999@gmail.com" class="connect-button">
                    📧 j9610577999@gmail.com
                </a>
                <a href="https://www.linkedin.com/in/jharna-saxena-502a6a2ba" class="connect-button">
                    💼 LinkedIn Profile
                </a>
            </div>
        </div>
        
        <!-- INSPIRATIONAL QUOTE -->
        <div class="quote-box">
            <p class="quote-text">
                "From a hesitant freshman who almost didn't apply, to a REYES mentee at Berkeley — 
                this journey taught me that you're just one YES away from a life-changing experience. 
                Never underestimate the power of showing up, even when you feel underqualified. 
                The magic happens outside your comfort zone! 🌸✨"
            </p>
        </div>
        
        <!-- FOOTER -->
        <div class="footer">
            <p>Made with 💖, pastel colors, and a sprinkle of Berkeley magic</p>
            <p>Last updated: December 2025 | Fiat Lux ✨</p>
            <p style="margin-top: 20px; font-size: 0.9em; color: #ff99bb;">
                ⭐ If you like my profile, feel free to star some repos! ⭐
            </p>
        </div>
    </div>
    
    <script>
        // Simple hover effects
        document.querySelectorAll('.timeline-item, .project-link, .badge').forEach(item => {
            item.addEventListener('mouseenter', function() {
                this.style.transform = 'translateY(-8px)';
            });
            item.addEventListener('mouseleave', function() {
                this.style.transform = 'translateY(0)';
            });
        });
        
        // Add sparkle animation
        function addSparkles() {
            const sparkles = ['✨', '🌸', '🎀', '💖', '🌟', '🦋'];
            const container = document.querySelector('.container');
            
            for(let i = 0; i < 15; i++) {
                const sparkle = document.createElement('div');
                sparkle.textContent = sparkles[Math.floor(Math.random() * sparkles.length)];
                sparkle.style.position = 'absolute';
                sparkle.style.left = Math.random() * 100 + '%';
                sparkle.style.top = Math.random() * 100 + '%';
                sparkle.style.opacity = '0.1';
                sparkle.style.fontSize = (Math.random() * 20 + 15) + 'px';
                sparkle.style.zIndex = '1';
                sparkle.style.pointerEvents = 'none';
                sparkle.style.animation = `float ${Math.random() * 5 + 3}s ease-in-out infinite`;
                sparkle.style.animationDelay = Math.random() * 2 + 's';
                container.appendChild(sparkle);
            }
        }
        
        // Add sparkles on load
        window.addEventListener('load', addSparkles);
    </script>
</body>
</html>
