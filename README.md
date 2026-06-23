<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Deepak Verma · GitHub Profile README</title>
    <!-- Font Awesome Icons (free version) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #0d1117;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            font-family: 'Segoe UI', 'Inter', system-ui, -apple-system, sans-serif;
            padding: 2rem 1rem;
        }

        /* Card container – simulates GitHub README feel */
        .readme-card {
            max-width: 880px;
            width: 100%;
            background: #161b22;
            border-radius: 24px;
            padding: 2.5rem 2.2rem;
            box-shadow: 0 20px 40px -12px rgba(0, 0, 0, 0.8);
            border: 1px solid #30363d;
            transition: all 0.2s ease;
        }

        /* ---------- ANIMATED BADGE / HEADER ---------- */
        .badge-animated {
            display: inline-flex;
            align-items: center;
            gap: 0.6rem;
            background: #1f2937;
            padding: 0.4rem 1rem 0.4rem 0.8rem;
            border-radius: 40px;
            font-size: 0.85rem;
            font-weight: 500;
            color: #f0f6fc;
            border: 1px solid #2d3748;
            margin-bottom: 1.8rem;
            letter-spacing: 0.3px;
            backdrop-filter: blur(2px);
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.3);
        }

        .badge-animated i {
            color: #58a6ff;
            font-size: 1rem;
            animation: pulseGlow 2.2s infinite ease-in-out;
        }

        .badge-animated .username {
            color: #f0f6fc;
            font-weight: 600;
        }

        .badge-animated .highlight {
            color: #f0883e;
            font-weight: 600;
        }

        @keyframes pulseGlow {
            0% { opacity: 0.6; transform: scale(0.96); }
            50% { opacity: 1; transform: scale(1.1); color: #f0883e; }
            100% { opacity: 0.6; transform: scale(0.96); }
        }

        /* ---------- TITLE & SUB ---------- */
        .profile-title {
            font-size: 2.8rem;
            font-weight: 700;
            color: #f0f6fc;
            letter-spacing: -0.02em;
            line-height: 1.2;
            display: flex;
            flex-wrap: wrap;
            align-items: baseline;
            gap: 0.4rem 0.8rem;
            margin-bottom: 0.25rem;
        }

        .profile-title .first-name {
            background: linear-gradient(135deg, #f0883e, #f6a85b);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .profile-title .last-name {
            color: #e6edf3;
        }

        .profile-title .wave {
            display: inline-block;
            animation: waveHand 2.8s infinite;
            transform-origin: 70% 70%;
            font-size: 2.8rem;
            line-height: 1;
            margin-left: 0.15rem;
        }

        @keyframes waveHand {
            0% { transform: rotate(0deg); }
            10% { transform: rotate(16deg); }
            20% { transform: rotate(-4deg); }
            30% { transform: rotate(16deg); }
            40% { transform: rotate(-2deg); }
            50% { transform: rotate(10deg); }
            60%, 100% { transform: rotate(0deg); }
        }

        .sub-git {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 0.6rem 1.2rem;
            margin-top: 0.1rem;
            margin-bottom: 1.8rem;
            color: #8b949e;
            font-size: 1.1rem;
            border-left: 3px solid #f0883e;
            padding-left: 1.2rem;
        }

        .sub-git i {
            color: #58a6ff;
            margin-right: 4px;
        }

        .sub-git .git-user {
            background: #21262d;
            padding: 0.2rem 0.9rem;
            border-radius: 30px;
            font-family: 'Fira Code', monospace;
            font-size: 0.95rem;
            color: #f0f6fc;
            border: 1px solid #30363d;
        }

        /* ---------- BIO / ABOUT ---------- */
        .bio-section {
            background: #0d1117;
            border-radius: 16px;
            padding: 1.5rem 1.8rem;
            margin: 1.8rem 0 2rem;
            border-left: 6px solid #f0883e;
            border-right: 1px solid #30363d;
            border-top: 1px solid #30363d;
            border-bottom: 1px solid #30363d;
            box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.4);
        }

        .bio-section p {
            color: #c9d1d9;
            font-size: 1.08rem;
            line-height: 1.6;
            display: flex;
            align-items: flex-start;
            gap: 0.8rem;
        }

        .bio-section p i {
            color: #f0883e;
            font-size: 1.5rem;
            margin-top: 0.2rem;
        }

        /* ---------- STATS / SKILLS GRID ---------- */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1.2rem;
            margin: 2.2rem 0 2rem;
        }

        .stat-item {
            background: #0d1117;
            padding: 1rem 1rem 1rem 1.4rem;
            border-radius: 40px;
            border: 1px solid #30363d;
            display: flex;
            align-items: center;
            gap: 0.8rem;
            transition: 0.2s ease;
            box-shadow: 0 4px 6px -4px rgba(0,0,0,0.5);
        }

        .stat-item:hover {
            border-color: #f0883e;
            transform: translateY(-3px);
            box-shadow: 0 8px 14px -6px #f0883e33;
        }

        .stat-item i {
            font-size: 1.6rem;
            color: #f0883e;
            width: 2rem;
            text-align: center;
        }

        .stat-item .stat-text {
            display: flex;
            flex-direction: column;
        }

        .stat-item .stat-label {
            font-size: 0.7rem;
            text-transform: uppercase;
            letter-spacing: 0.6px;
            color: #8b949e;
        }

        .stat-item .stat-value {
            font-weight: 600;
            color: #f0f6fc;
            font-size: 1.1rem;
        }

        /* ---------- TOOLS / TECH (animated icons) ---------- */
        .tech-section {
            margin: 2.2rem 0 1.8rem;
        }

        .tech-section h3 {
            color: #f0f6fc;
            font-size: 1.2rem;
            font-weight: 500;
            letter-spacing: 0.3px;
            display: flex;
            align-items: center;
            gap: 0.7rem;
            margin-bottom: 1.2rem;
        }

        .tech-section h3 i {
            color: #f0883e;
            animation: pulseGlow 2.8s infinite;
        }

        .tech-icons {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem 1.8rem;
            align-items: center;
        }

        .tech-icons span {
            background: #21262d;
            padding: 0.4rem 1.2rem;
            border-radius: 40px;
            font-size: 0.95rem;
            font-weight: 500;
            color: #e6edf3;
            border: 1px solid #30363d;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            transition: 0.2s;
            box-shadow: 0 2px 4px rgba(0,0,0,0.3);
        }

        .tech-icons span i {
            color: #f0883e;
            font-size: 1.1rem;
        }

        .tech-icons span:hover {
            border-color: #f0883e;
            background: #1f2937;
            transform: scale(1.02) translateY(-2px);
            box-shadow: 0 8px 12px -6px #f0883e33;
        }

        /* ---------- SOCIAL / LINKS (animated) ---------- */
        .social-links {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 1rem 1.8rem;
            padding-top: 1.2rem;
            margin-top: 1.2rem;
            border-top: 1px solid #30363d;
        }

        .social-links a {
            color: #8b949e;
            font-size: 1.3rem;
            transition: 0.25s ease;
            display: inline-flex;
            align-items: center;
            gap: 0.4rem;
            text-decoration: none;
            background: #0d1117;
            padding: 0.3rem 1rem 0.3rem 0.9rem;
            border-radius: 40px;
            border: 1px solid #21262d;
        }

        .social-links a i {
            font-size: 1.5rem;
            width: 2rem;
            text-align: center;
        }

        .social-links a .handle {
            font-size: 0.8rem;
            font-weight: 400;
            letter-spacing: 0.2px;
        }

        .social-links a:hover {
            color: #f0f6fc;
            border-color: #f0883e;
            background: #1f2937;
            transform: translateY(-3px);
            box-shadow: 0 6px 12px -4px #f0883e44;
        }

        .social-links a:hover i {
            color: #f0883e;
        }

        /* ---------- FOOTER NOTE ---------- */
        .footer-note {
            margin-top: 2.2rem;
            color: #484f58;
            font-size: 0.8rem;
            display: flex;
            justify-content: flex-end;
            border-top: 1px solid #21262d;
            padding-top: 1.2rem;
            letter-spacing: 0.3px;
        }

        .footer-note i {
            color: #f0883e;
            margin: 0 4px;
        }

        /* Responsive */
        @media (max-width: 600px) {
            .readme-card {
                padding: 1.8rem 1.2rem;
            }
            .profile-title {
                font-size: 2.2rem;
            }
            .profile-title .wave {
                font-size: 2.2rem;
            }
            .sub-git {
                font-size: 0.95rem;
                padding-left: 0.8rem;
            }
            .stats-grid {
                grid-template-columns: 1fr 1fr;
            }
            .bio-section p {
                font-size: 1rem;
                flex-wrap: wrap;
            }
        }
    </style>
</head>
<body>
    <div class="readme-card">
        <!-- Animated badge: git username + name -->
        <div class="badge-animated">
            <i class="fas fa-code-branch"></i>
            <span><span class="username">Deepakkumar7009</span> · <span class="highlight">Deepak Verma</span></span>
            <i class="fas fa-circle" style="font-size: 0.5rem; color: #3fb950; animation: none; margin-left: 0.2rem;"></i>
        </div>

        <!-- Title with waving hand animation -->
        <div class="profile-title">
            <span class="first-name">Deepak</span>
            <span class="last-name">Verma</span>
            <span class="wave">👋</span>
        </div>

        <!-- Git username + location / status -->
        <div class="sub-git">
            <span><i class="fas fa-user-astronaut"></i> @Deepakkumar7009</span>
            <span><i class="fas fa-map-pin"></i> India · UTC +5:30</span>
            <span><i class="fas fa-code"></i> full-stack & devops</span>
            <span class="git-user"><i class="fab fa-github"></i> Deepakkumar7009</span>
        </div>

        <!-- Bio / about section -->
        <div class="bio-section">
            <p>
                <i class="fas fa-quote-left"></i>
                <span>Building things that matter. Passionate about clean code, cloud-native architectures, and turning complex problems into elegant solutions. <span style="color: #f0883e; font-weight: 500;">#craftsmanship</span></span>
            </p>
        </div>

        <!-- Animated stats / highlights -->
        <div class="stats-grid">
            <div class="stat-item">
                <i class="fas fa-rocket"></i>
                <div class="stat-text">
                    <span class="stat-label">Focus</span>
                    <span class="stat-value">Backend · DevOps</span>
                </div>
            </div>
            <div class="stat-item">
                <i class="fas fa-laptop-code"></i>
                <div class="stat-text">
                    <span class="stat-label">Experience</span>
                    <span class="stat-value">5+ years</span>
                </div>
            </div>
            <div class="stat-item">
                <i class="fas fa-users"></i>
                <div class="stat-text">
                    <span class="stat-label">Community</span>
                    <span class="stat-value">Open Source</span>
                </div>
            </div>
            <div class="stat-item">
                <i class="fas fa-award"></i>
                <div class="stat-text">
                    <span class="stat-label">Projects</span>
                    <span class="stat-value">15+ public</span>
                </div>
            </div>
        </div>

        <!-- Tech / tools with animated icons -->
        <div class="tech-section">
            <h3>
                <i class="fas fa-cog fa-spin" style="--fa-animation-duration: 6s;"></i>
                tech stack & tools
            </h3>
            <div class="tech-icons">
                <span><i class="fab fa-python"></i> Python</span>
                <span><i class="fab fa-js"></i> JavaScript</span>
                <span><i class="fab fa-golang"></i> Go</span>
                <span><i class="fas fa-database"></i> PostgreSQL</span>
                <span><i class="fab fa-docker"></i> Docker</span>
                <span><i class="fas fa-cloud"></i> AWS</span>
                <span><i class="fas fa-code-branch"></i> Git</span>
                <span><i class="fas fa-terminal"></i> Linux</span>
                <span><i class="fas fa-cubes"></i> Kubernetes</span>
            </div>
        </div>

        <!-- Social / links with animation on hover -->
        <div class="social-links">
            <a href="#" target="_blank">
                <i class="fab fa-github"></i>
                <span class="handle">Deepakkumar7009</span>
            </a>
            <a href="#" target="_blank">
                <i class="fab fa-linkedin-in"></i>
                <span class="handle">deepak-verma</span>
            </a>
            <a href="#" target="_blank">
                <i class="fab fa-twitter"></i>
                <span class="handle">@deepak_dev</span>
            </a>
            <a href="#" target="_blank">
                <i class="fas fa-envelope"></i>
                <span class="handle">deepak@devmail</span>
            </a>
            <a href="#" target="_blank">
                <i class="fas fa-globe"></i>
                <span class="handle">deepak.dev</span>
            </a>
        </div>

        <!-- small animated footer -->
        <div class="footer-note">
            <span><i class="fas fa-arrow-right"></i> always building · <i class="fas fa-heart" style="color: #f0883e; animation: pulseGlow 1.8s infinite;"></i> open source</span>
        </div>
    </div>
</body>
</html>
