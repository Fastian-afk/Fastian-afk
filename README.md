<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Imaad Fazal - GitHub Profile</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
            background-attachment: fixed;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            color: #fff;
            overflow-x: hidden;
            min-height: 100vh;
            padding: 40px 20px;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
        }

        /* Animated Background */
        @keyframes gradientShift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        /* Glowing Text Animation */
        @keyframes glowPulse {
            0%, 100% { text-shadow: 0 0 10px #00d4ff, 0 0 20px #0099ff; }
            50% { text-shadow: 0 0 20px #00d4ff, 0 0 40px #0099ff, 0 0 60px #ff00ff; }
        }

        @keyframes slideInLeft {
            from {
                opacity: 0;
                transform: translateX(-50px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        @keyframes slideInRight {
            from {
                opacity: 0;
                transform: translateX(50px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes typewriter {
            from {
                width: 0;
                opacity: 1;
            }
            to {
                width: 100%;
                opacity: 1;
            }
        }

        @keyframes blink {
            0%, 50% { border-right-color: #00d4ff; }
            51%, 100% { border-right-color: transparent; }
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        @keyframes rainbow {
            0% { color: #ff0000; }
            16% { color: #ff7f00; }
            33% { color: #ffff00; }
            50% { color: #00ff00; }
            66% { color: #0000ff; }
            83% { color: #4b0082; }
            100% { color: #ff0000; }
        }

        /* Hero Section */
        .hero {
            text-align: center;
            margin-bottom: 60px;
            animation: fadeInUp 1s ease-out;
        }

        .hero h1 {
            font-size: 4rem;
            font-weight: 900;
            margin-bottom: 10px;
            animation: glowPulse 2s infinite, slideInLeft 0.8s ease-out;
            background: linear-gradient(135deg, #00d4ff, #ff00ff, #00d4ff);
            background-size: 200% 200%;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: glowPulse 2s infinite, slideInLeft 0.8s ease-out, gradientShift 3s infinite;
        }

        .typing-text {
            font-size: 1.8rem;
            margin-top: 15px;
            min-height: 50px;
            animation: slideInRight 1s ease-out;
        }

        .typing-text span {
            display: inline-block;
            border-right: 3px solid #00d4ff;
            animation: typewriter 3s steps(30, end) 0.5s 1 normal both, blink 0.7s infinite 3s;
            white-space: nowrap;
            overflow: hidden;
        }

        /* Emoji Float */
        .emoji-float {
            display: inline-block;
            animation: float 3s infinite;
            font-size: 2.5rem;
            margin: 0 10px;
        }

        /* Links Section */
        .links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
            flex-wrap: wrap;
            animation: fadeInUp 1.2s ease-out;
        }

        .link-btn {
            padding: 12px 25px;
            background: linear-gradient(135deg, #667eea, #764ba2);
            border: 2px solid #00d4ff;
            color: #fff;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            transition: all 0.3s ease;
            cursor: pointer;
            position: relative;
            overflow: hidden;
            font-size: 0.95rem;
        }

        .link-btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, #00d4ff, #ff00ff);
            transition: left 0.3s ease;
            z-index: -1;
        }

        .link-btn:hover::before {
            left: 0;
        }

        .link-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0, 212, 255, 0.5);
        }

        /* Section Styles */
        .section {
            margin-bottom: 50px;
            animation: fadeInUp 1s ease-out;
        }

        .section h2 {
            font-size: 2.5rem;
            margin-bottom: 25px;
            animation: slideInLeft 0.8s ease-out;
            color: #00d4ff;
            text-shadow: 0 0 10px #00d4ff;
            position: relative;
            display: inline-block;
        }

        .section h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 0;
            width: 100%;
            height: 3px;
            background: linear-gradient(90deg, #00d4ff, #ff00ff, transparent);
            animation: slideInRight 0.8s ease-out;
        }

        .content-box {
            background: rgba(48, 43, 99, 0.3);
            border: 2px solid #00d4ff;
            border-radius: 15px;
            padding: 30px;
            margin: 20px 0;
            backdrop-filter: blur(10px);
            animation: fadeInUp 0.8s ease-out;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .content-box::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -50%;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle, rgba(0, 212, 255, 0.1) 0%, transparent 70%);
            animation: spin 20s linear infinite;
        }

        .content-box:hover {
            border-color: #ff00ff;
            box-shadow: 0 0 20px rgba(255, 0, 255, 0.3);
            transform: translateY(-5px);
        }

        .content-box > * {
            position: relative;
            z-index: 2;
        }

        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 15px;
            margin: 20px 0;
        }

        .tech-item {
            background: linear-gradient(135deg, #667eea, #764ba2);
            padding: 20px;
            border-radius: 10px;
            text-align: center;
            font-weight: bold;
            transition: all 0.3s ease;
            animation: fadeInUp 0.8s ease-out;
            border: 2px solid transparent;
            cursor: pointer;
        }

        .tech-item:hover {
            border-color: #00d4ff;
            transform: scale(1.05) rotate(5deg);
            box-shadow: 0 0 20px rgba(0, 212, 255, 0.5);
        }

        .project-card {
            background: linear-gradient(135deg, rgba(102, 126, 234, 0.2), rgba(118, 75, 162, 0.2));
            border: 2px solid #00d4ff;
            border-radius: 12px;
            padding: 25px;
            margin: 20px 0;
            animation: fadeInUp 0.8s ease-out;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(0, 212, 255, 0.2), transparent);
            transition: left 0.5s ease;
        }

        .project-card:hover::before {
            left: 100%;
        }

        .project-card:hover {
            border-color: #ff00ff;
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0, 212, 255, 0.3);
        }

        .project-card h3 {
            font-size: 1.5rem;
            margin-bottom: 10px;
            color: #00d4ff;
            animation: rainbow 3s infinite;
        }

        .project-card p {
            color: #ccc;
            line-height: 1.6;
            margin-bottom: 10px;
        }

        .stat-badge {
            display: inline-block;
            background: linear-gradient(135deg, #ff00ff, #00d4ff);
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: bold;
            margin: 5px 5px 5px 0;
            animation: fadeInUp 0.8s ease-out;
        }

        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin: 20px 0;
        }

        .stat-box {
            background: linear-gradient(135deg, #667eea, #764ba2);
            padding: 25px;
            border-radius: 10px;
            text-align: center;
            animation: float 3s infinite;
            border: 2px solid #00d4ff;
            transition: all 0.3s ease;
        }

        .stat-box:hover {
            transform: scale(1.05);
            box-shadow: 0 0 20px rgba(0, 212, 255, 0.5);
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: 900;
            color: #ff00ff;
            animation: rainbow 3s infinite;
        }

        .stat-label {
            font-size: 0.9rem;
            color: #00d4ff;
            margin-top: 10px;
        }

        .footer {
            text-align: center;
            padding: 40px 20px;
            color: #00d4ff;
            animation: glowPulse 2s infinite;
            font-size: 1.2rem;
            margin-top: 60px;
        }

        .divider {
            height: 3px;
            background: linear-gradient(90deg, transparent, #00d4ff, #ff00ff, transparent);
            margin: 40px 0;
            animation: slideInRight 0.8s ease-out;
        }

        /* Delay animations */
        .delay-1 { animation-delay: 0.1s; }
        .delay-2 { animation-delay: 0.2s; }
        .delay-3 { animation-delay: 0.3s; }
        .delay-4 { animation-delay: 0.4s; }
        .delay-5 { animation-delay: 0.5s; }
    </style>
</head>
<body>
    <div class="container">
        <!-- Hero Section -->
        <div class="hero">
            <h1>
                <span class="emoji-float">🚀</span>
                <span class="typing-text"><span>Yo, I'm Imaad Fazal</span></span>
                <span class="emoji-float">⚡</span>
            </h1>
            <div class="typing-text" style="margin-top: 20px; font-size: 1.5rem;">
                <span style="animation-delay: 3.5s;">AI/ML Engineer • Healthcare Tech • Data Wizard</span>
            </div>
        </div>

        <div class="links">
            <a href="https://imaad-fazal-portfolio-hub.vercel.app/" class="link-btn delay-1">🌐 Portfolio</a>
            <a href="https://www.linkedin.com/in/imaad-fazal-30a096320/" class="link-btn delay-2">💼 LinkedIn</a>
            <a href="mailto:imdufazal@gmail.com" class="link-btn delay-3">📧 Email</a>
            <a href="https://github.com/Fastian-afk" class="link-btn delay-4">💻 GitHub</a>
        </div>

        <div class="divider"></div>

        <!-- About Me -->
        <div class="section delay-1">
            <h2>✨ Who tf am I? 💫</h2>
            <div class="content-box">
                <p style="font-size: 1.1rem; line-height: 1.8; margin-bottom: 20px;">
                    🧠 Not your average AI student... Building interpretable ML models that actually make sense
                </p>
                <p style="font-size: 1.1rem; line-height: 1.8; margin-bottom: 20px;">
                    🏥 Obsessed with medical AI, SHAP explainability, and real-world impact (no cap)
                </p>
                <p style="font-size: 1.1rem; line-height: 1.8; margin-bottom: 20px;">
                    🎯 Portfolio-grade projects only, none of that tutorial slop
                </p>
                <p style="font-size: 1.1rem; line-height: 1.8;">
                    💎 Python wizard • Deep learning enthusiast • Data pipeline architect
                </p>
            </div>
        </div>

        <div class="divider"></div>

        <!-- Tech Stack -->
        <div class="section delay-2">
            <h2>🛠️ My Arsenal 🔥</h2>
            <div class="content-box">
                <p style="margin-bottom: 20px; font-size: 1rem;">Languages I spit flames with 🔥</p>
                <div class="tech-grid">
                    <div class="tech-item delay-1">🐍 Python</div>
                    <div class="tech-item delay-2">⚙️ C++</div>
                    <div class="tech-item delay-3">☕ Java</div>
                </div>

                <p style="margin: 30px 0 20px 0; font-size: 1rem;">ML/DL Frameworks that hit different 🎯</p>
                <div class="tech-grid">
                    <div class="tech-item delay-1">🔷 TensorFlow</div>
                    <div class="tech-item delay-2">🔥 PyTorch</div>
                    <div class="tech-item delay-3">📊 Scikit-Learn</div>
                </div>

                <p style="margin: 30px 0 20px 0; font-size: 1rem;">Tools & Platforms I vibe with 💫</p>
                <div class="tech-grid">
                    <div class="tech-item delay-1">📓 Jupyter</div>
                    <div class="tech-item delay-2">🌳 Git</div>
                    <div class="tech-item delay-3">🐙 GitHub</div>
                    <div class="tech-item delay-4">💻 VS Code</div>
                </div>
            </div>
        </div>

        <div class="divider"></div>

        <!-- Projects -->
        <div class="section delay-3">
            <h2>🚀 Main Character Energy Projects 💀</h2>
            <div class="content-box">
                <div class="project-card delay-1">
                    <h3>🫁 Pneumonia Detection</h3>
                    <p>Grad-CAM + ResNet18 | Medical imaging that's interpretable AF</p>
                    <div>
                        <span class="stat-badge">Deep Learning</span>
                        <span class="stat-badge">Computer Vision</span>
                        <span class="stat-badge">Explainable AI</span>
                    </div>
                </div>

                <div class="project-card delay-2">
                    <h3>🩺 Heart Disease Prediction</h3>
                    <p>Interpretable ML with SHAP | Features that actually make sense</p>
                    <div>
                        <span class="stat-badge">Healthcare</span>
                        <span class="stat-badge">SHAP</span>
                        <span class="stat-badge">Interpretability</span>
                    </div>
                </div>

                <div class="project-card delay-3">
                    <h3>🧬 Sepsis Prediction (MIMIC)</h3>
                    <p>Clinical data pipeline | Real hospital data, real problems</p>
                    <div>
                        <span class="stat-badge">Time Series</span>
                        <span class="stat-badge">Clinical Data</span>
                        <span class="stat-badge">Prediction</span>
                    </div>
                </div>

                <div class="project-card delay-4">
                    <h3>🎵 Smart Music Recommender</h3>
                    <p>ML-based recommendations | Vibes personalized just for you</p>
                    <div>
                        <span class="stat-badge">Recommendation Engine</span>
                        <span class="stat-badge">Collaborative Filtering</span>
                        <span class="stat-badge">ML</span>
                    </div>
                </div>
            </div>
        </div>

        <div class="divider"></div>

        <!-- Stats -->
        <div class="section delay-4">
            <h2>📈 The Numbers Don't Lie 💯</h2>
            <div class="stats-container">
                <div class="stat-box delay-1">
                    <div class="stat-number">15+</div>
                    <div class="stat-label">Projects Built</div>
                </div>
                <div class="stat-box delay-2">
                    <div class="stat-number">3</div>
                    <div class="stat-label">Languages</div>
                </div>
                <div class="stat-box delay-3">
                    <div class="stat-number">8+</div>
                    <div class="stat-label">ML Frameworks</div>
                </div>
                <div class="stat-box delay-4">
                    <div class="stat-number">100%</div>
                    <div class="stat-label">Portfolio Grade</div>
                </div>
            </div>
        </div>

        <div class="divider"></div>

        <!-- Currently Exploring -->
        <div class="section delay-5">
            <h2>🔮 What I'm Grinding On RN 👀</h2>
            <div class="content-box">
                <div class="tech-grid">
                    <div class="tech-item delay-1">🔬 Medical AI & Explainability</div>
                    <div class="tech-item delay-2">📈 End-to-End ML Pipelines</div>
                    <div class="tech-item delay-3">☁️ Cloud Deployment (AWS/GCP)</div>
                    <div class="tech-item delay-4">📱 Edge Deployment</div>
                    <div class="tech-item delay-5">🤝 Open Source Contributions</div>
                </div>
            </div>
        </div>

        <div class="divider"></div>

        <!-- Footer -->
        <div class="footer">
            <p style="margin-bottom: 20px; font-size: 1.5rem;">
                Let's build something that actually matters 🚀
            </p>
            <p style="color: #ff00ff;">
                DM me • Connect on LinkedIn • Check out my repos
            </p>
        </div>
    </div>
</body>
</html>
