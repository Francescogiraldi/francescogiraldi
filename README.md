<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Francesco Giraldi - AI & Data Specialist</title>
    <style>
        /* Japanese-inspired color palette */
        :root {
            --sakura-pink: #f8c3cd;
            --washi-cream: #f5f5f0;
            --sumi-black: #1a1a1a;
            --enji-red: #e95464;
            --wave-blue: #7db4d6;
            --gold-accent: #d4af37;
        }

        body {
            background-color: var(--washi-cream);
            color: var(--sumi-black);
            font-family: 'Noto Sans JP', 'Helvetica Neue', Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 0;
            background-image: 
                url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><path fill="%23f8c3cd" fill-opacity="0.1" d="M30,10 Q50,5 70,10 T90,30 Q95,50 90,70 T70,90 Q50,95 30,90 T10,70 Q5,50 10,30 T30,10 Z"/></svg>');
            background-size: 200px;
        }

        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 40px;
            position: relative;
            overflow: hidden;
        }

        .container::before {
            content: "";
            position: absolute;
            top: 0;
            right: 0;
            width: 300px;
            height: 300px;
            background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><path fill="%237db4d6" fill-opacity="0.2" d="M0,50 C20,10 40,30 60,20 S100,40 100,50 S80,90 60,80 S0,90 0,50 Z"/></svg>');
            background-repeat: no-repeat;
            z-index: -1;
        }

        h1, h2, h3 {
            color: var(--enji-red);
            font-weight: 700;
            letter-spacing: 1px;
        }

        h1 {
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 10px;
            position: relative;
        }

        h1::after {
            content: "";
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 3px;
            background: linear-gradient(90deg, var(--enji-red), var(--gold-accent), var(--enji-red));
        }

        .tagline {
            text-align: center;
            font-size: 1.2rem;
            margin-bottom: 40px;
            color: var(--sumi-black);
            position: relative;
        }

        .tagline::before, .tagline::after {
            content: "❀";
            color: var(--sakura-pink);
            margin: 0 10px;
        }

        .section {
            margin-bottom: 40px;
            padding: 20px;
            background-color: rgba(255, 255, 255, 0.8);
            border-radius: 5px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
            position: relative;
            overflow: hidden;
        }

        .section::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 100%;
            background: linear-gradient(to bottom, var(--enji-red), var(--gold-accent));
        }

        .mission-statement {
            font-family: 'Courier New', monospace;
            background-color: rgba(245, 245, 240, 0.7);
            padding: 15px;
            border-left: 3px solid var(--enji-red);
            margin: 15px 0;
        }

        .quote {
            font-style: italic;
            color: var(--sumi-black);
            padding: 10px 20px;
            border-radius: 5px;
            background-color: rgba(248, 195, 205, 0.2);
            position: relative;
        }

        .quote::before {
            content: "“";
            font-size: 3rem;
            color: var(--sakura-pink);
            position: absolute;
            left: -5px;
            top: -15px;
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }

        .project-card {
            background-color: white;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
            transition: all 0.3s;
            border-top: 3px solid var(--wave-blue);
        }

        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }

        .project-icon {
            font-size: 1.5rem;
            margin-right: 10px;
            color: var(--enji-red);
        }

        .connect-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
        }

        .connect-link {
            background-color: var(--enji-red);
            color: white;
            padding: 10px 20px;
            border-radius: 30px;
            text-decoration: none;
            transition: all 0.3s;
            display: flex;
            align-items: center;
        }

        .connect-link:hover {
            background-color: var(--sumi-black);
            transform: translateY(-3px);
        }

        .connect-link::before {
            content: "→";
            margin-right: 5px;
        }

        footer {
            text-align: center;
            margin-top: 40px;
            padding: 20px;
            color: var(--sumi-black);
            position: relative;
        }

        footer::before {
            content: "";
            position: absolute;
            top: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 200px;
            height: 2px;
            background: linear-gradient(90deg, transparent, var(--wave-blue), transparent);
        }

        /* Cherry blossom animation */
        .cherry-blossom {
            position: fixed;
            width: 20px;
            height: 20px;
            background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><path fill="%23f8c3cd" d="M50,10 Q55,0 60,10 T70,20 Q80,25 70,30 T60,40 Q55,50 50,40 T40,30 Q30,25 40,20 T50,10 Z"/></svg>');
            background-size: contain;
            pointer-events: none;
            z-index: 9998;
            animation: falling linear infinite;
        }

        @keyframes falling {
            0% {
                transform: translateY(-10vh) rotate(0deg);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            90% {
                opacity: 1;
            }
            100% {
                transform: translateY(110vh) rotate(360deg);
                opacity: 0;
            }
        }

        /* Responsive design */
        @media (max-width: 768px) {
            .container {
                padding: 20px;
            }
            
            h1 {
                font-size: 2rem;
            }
            
            .projects-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@300;400;500;700&display=swap" rel="stylesheet">
</head>
<body>
    <div id="cherry-blossom-container"></div>
    
    <div class="container">
        <h1>👾 HI, I'M FRANCESCO GIRALDI</h1>
        
        <div class="tagline">
            MAKE DATA & AI EASY · SIMPLIFY COMPLEXITY
        </div>

        <div class="section">
            <h2>🚀 MISSION</h2>
            <div class="mission-statement">
                S I M P L I F Y   C O M P L E X I T Y<br>
                E M P O W E R   P E O P L E<br>
                I M P R O V E   T H E   W O R L D<br>
                T H R O U G H   D A T A   &   A I
            </div>
            <ul>
                <li>🔍 Understandable AI for everyone</li>
                <li>🧭 Data into human language and storytelling</li>
                <li>💡 Complexity into Clarity</li>
            </ul>
        </div>

        <div class="section">
            <h2>🛠️ WHAT I DO</h2>
            <div class="mission-statement">
                🎯  B U I L D    S I M P L E   A I   T O O L S<br>
                📊  T U R N    D A T A   I N T O   S T O R I E S<br>
                🤝  M A K E    T E C H N O L O G Y   H U M A N
            </div>
            <div class="quote">
                "If you can't explain it to a 10-year-old, you don't understand it enough."
            </div>
        </div>

        <div class="section">
            <h2>💡 FEATURED PROJECTS</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <h3><span class="project-icon">🌸</span> IKIGAI PRO</h3>
                    <p>AI for personal growth and self-discovery</p>
                </div>
                <div class="project-card">
                    <h3><span class="project-icon">🌊</span> MICHELIN TIRE HUNT</h3>
                    <p>Gamifying complex product data for better decisions</p>
                </div>
                <div class="project-card">
                    <h3><span class="project-icon">📘</span> EASY DATA GUIDES</h3>
                    <p>Visual AI guides anyone can follow</p>
                </div>
            </div>
        </div>

        <div class="section">
            <h2>🔗 CONNECT</h2>
            <div class="connect-links">
                <a href="https://linkedin.com/in/francescogiraldi" class="connect-link">LINKEDIN</a>
                <a href="https://francescogiraldi.dev" class="connect-link">PORTFOLIO</a>
                <a href="mailto:francesco@gmail.com" class="connect-link">EMAIL</a>
            </div>
        </div>

        <footer>
            <p>AI & DATA FOR HUMANS</p>
        </footer>
    </div>

    <script>
        // Create cherry blossoms
        function createCherryBlossoms() {
            const container = document.getElementById('cherry-blossom-container');
            const numBlossoms = 15;
            
            for (let i = 0; i < numBlossoms; i++) {
                const blossom = document.createElement('div');
                blossom.className = 'cherry-blossom';
                
                // Random properties
                const size = Math.random() * 15 + 10;
                const left = Math.random() * 100;
                const animationDuration = Math.random() * 10 + 10;
                const delay = Math.random() * 15;
                
                blossom.style.width = `${size}px`;
                blossom.style.height = `${size}px`;
                blossom.style.left = `${left}vw`;
                blossom.style.animationDuration = `${animationDuration}s`;
                blossom.style.animationDelay = `${delay}s`;
                blossom.style.opacity = Math.random() * 0.5 + 0.3;
                
                container.appendChild(blossom);
            }
        }

        document.addEventListener('DOMContentLoaded', createCherryBlossoms);
    </script>
</body>
</html>

