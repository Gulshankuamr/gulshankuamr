
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gulshan Kumar - Frontend Developer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background-color: #0d1117;
            color: #c9d1d9;
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Helvetica Neue', Arial, sans-serif;
            line-height: 1.6;
            padding: 20px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        /* Header Section */
        .header {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            margin-bottom: 60px;
            padding-bottom: 40px;
            border-bottom: 1px solid #30363d;
        }

        .profile-info h1 {
            font-size: 2.5rem;
            color: #00ff41;
            margin-bottom: 10px;
            text-shadow: 0 0 10px rgba(0, 255, 65, 0.3);
        }

        .profile-info p {
            font-size: 1.1rem;
            color: #8b949e;
            margin-bottom: 20px;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
        }

        .stat-item {
            background: #161b22;
            padding: 15px;
            border-radius: 8px;
            border-left: 3px solid #00ff41;
        }

        .stat-value {
            font-size: 1.5rem;
            color: #00ff41;
            font-weight: bold;
        }

        .stat-label {
            color: #8b949e;
            font-size: 0.9rem;
            margin-top: 5px;
        }

        .metrics {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 15px;
        }

        .metric-box {
            background: #161b22;
            padding: 20px;
            border-radius: 8px;
            text-align: center;
            border: 1px solid #30363d;
        }

        .metric-score {
            font-size: 2rem;
            color: #00ff41;
            font-weight: bold;
            margin-bottom: 8px;
        }

        .metric-label {
            font-size: 0.85rem;
            color: #8b949e;
        }

        /* Tech Stack Section */
        .tech-section {
            margin-bottom: 60px;
        }

        .section-title {
            font-size: 1.5rem;
            color: #f0883e;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .section-title::before {
            content: "🔥";
        }

        .tech-categories {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }

        .tech-category {
            background: #161b22;
            padding: 20px;
            border-radius: 8px;
            border: 1px solid #30363d;
        }

        .tech-category h3 {
            color: #00ff41;
            margin-bottom: 15px;
            font-size: 1rem;
        }

        .tech-list {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
        }

        .tech-tag {
            background: #0d1117;
            border: 1px solid #00ff41;
            color: #00ff41;
            padding: 6px 12px;
            border-radius: 20px;
            font-size: 0.85rem;
        }

        /* Languages Chart */
        .languages {
            margin-bottom: 60px;
        }

        .languages h3 {
            color: #f0883e;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .languages h3::before {
            content: "💬";
        }

        .language-item {
            margin-bottom: 15px;
        }

        .language-name {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
            color: #c9d1d9;
        }

        .language-bar {
            height: 8px;
            background: #30363d;
            border-radius: 4px;
            overflow: hidden;
        }

        .language-fill {
            height: 100%;
            background: linear-gradient(90deg, #00ff41, #00cc33);
            border-radius: 4px;
        }

        /* Contributions Calendar */
        .contributions {
            background: #161b22;
            padding: 20px;
            border-radius: 8px;
            margin-bottom: 60px;
            border: 1px solid #30363d;
        }

        .contributions h3 {
            color: #00ff41;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .contributions h3::before {
            content: "📅";
        }

        .calendar-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(40px, 1fr));
            gap: 3px;
            margin-bottom: 20px;
        }

        .calendar-day {
            aspect-ratio: 1;
            background: #0d1117;
            border: 1px solid #30363d;
            border-radius: 3px;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .calendar-day:hover {
            border-color: #00ff41;
        }

        .calendar-day.active-1 {
            background: rgba(0, 255, 65, 0.2);
            border-color: #00ff41;
        }

        .calendar-day.active-2 {
            background: rgba(0, 255, 65, 0.5);
            border-color: #00ff41;
        }

        .calendar-day.active-3 {
            background: #00ff41;
        }

        /* About Section */
        .about {
            background: #161b22;
            padding: 30px;
            border-radius: 8px;
            border: 1px solid #30363d;
            margin-bottom: 60px;
        }

        .about h3 {
            color: #00ff41;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .about h3::before {
            content: "👋";
        }

        .about p {
            color: #8b949e;
            margin-bottom: 15px;
            line-height: 1.8;
        }

        /* Projects Section */
        .projects {
            margin-bottom: 60px;
        }

        .projects h3 {
            color: #f0883e;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .projects h3::before {
            content: "🚀";
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
        }

        .project-card {
            background: #161b22;
            padding: 20px;
            border-radius: 8px;
            border: 1px solid #30363d;
            transition: all 0.3s ease;
        }

        .project-card:hover {
            border-color: #00ff41;
            box-shadow: 0 0 15px rgba(0, 255, 65, 0.2);
        }

        .project-card h4 {
            color: #00ff41;
            margin-bottom: 10px;
        }

        .project-card p {
            color: #8b949e;
            font-size: 0.9rem;
        }

        /* Footer */
        footer {
            text-align: center;
            padding-top: 40px;
            border-top: 1px solid #30363d;
            color: #8b949e;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }

        .social-links a {
            color: #00ff41;
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .social-links a:hover {
            transform: scale(1.1);
            text-shadow: 0 0 10px rgba(0, 255, 65, 0.5);
        }

        /* Responsive */
        @media (max-width: 768px) {
            .header {
                grid-template-columns: 1fr;
            }

            .metrics {
                grid-template-columns: repeat(2, 1fr);
            }

            .profile-info h1 {
                font-size: 2rem;
            }

            .tech-categories {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header Section -->
        <div class="header">
            <div class="profile-info">
                <h1>✨ Gulshan Kumar ✨</h1>
                <p>Frontend Developer (React.js | Next.js)</p>
                <p>🚀 Passionate about building modern, responsive & high-performance web experiences</p>
                <p>🌍 From Lucknow, India | 💼 Frontend Developer | 🎨 UI/UX Enthusiast</p>
            </div>

            <div class="metrics">
                <div class="metric-box">
                    <div class="metric-score">97</div>
                    <div class="metric-label">Performance</div>
                </div>
                <div class="metric-box">
                    <div class="metric-score">100</div>
                    <div class="metric-label">Accessibility</div>
                </div>
                <div class="metric-box">
                    <div class="metric-score">100</div>
                    <div class="metric-label">Best Practices</div>
                </div>
                <div class="metric-box">
                    <div class="metric-score">100</div>
                    <div class="metric-label">SEO</div>
                </div>
            </div>
        </div>

        <!-- About Section -->
        <div class="about">
            <h3>About Me</h3>
            <p>Hi! I'm <strong>Gulshan Kumar</strong>, a dedicated <strong>Frontend Developer</strong> specializing in React.js, Next.js, Tailwind CSS & JavaScript (ES6+).</p>
            <p>I love turning ideas into <strong>clean, beautiful & functional web apps</strong> with animations, responsive layouts, and seamless user experiences.</p>
            <p><em>A fast learner with strong problem-solving skills and a passion for writing clean, maintainable code.</em></p>
        </div>

        <!-- Tech Stack Section -->
        <div class="tech-section">
            <h3 class="section-title">Tech Stack</h3>
            <div class="tech-categories">
                <div class="tech-category">
                    <h3>Frontend</h3>
                    <div class="tech-list">
                        <span class="tech-tag">React.js</span>
                        <span class="tech-tag">Next.js</span>
                        <span class="tech-tag">JavaScript</span>
                        <span class="tech-tag">ES6+</span>
                    </div>
                </div>

                <div class="tech-category">
                    <h3>Styling</h3>
                    <div class="tech-list">
                        <span class="tech-tag">Tailwind CSS</span>
                        <span class="tech-tag">Bootstrap</span>
                        <span class="tech-tag">CSS3</span>
                    </div>
                </div>

                <div class="tech-category">
                    <h3>Tools & APIs</h3>
                    <div class="tech-list">
                        <span class="tech-tag">Git</span>
                        <span class="tech-tag">GitHub</span>
                        <span class="tech-tag">REST APIs</span>
                        <span class="tech-tag">Axios</span>
                    </div>
                </div>

                <div class="tech-category">
                    <h3>Dev Tools</h3>
                    <div class="tech-list">
                        <span class="tech-tag">VS Code</span>
                        <span class="tech-tag">Chrome DevTools</span>
                        <span class="tech-tag">Figma</span>
                        <span class="tech-tag">Vercel</span>
                    </div>
                </div>
            </div>
        </div>

        <!-- Languages -->
        <div class="languages">
            <h3>Most Used Languages</h3>
            <div class="language-item">
                <div class="language-name">
                    <span>JavaScript</span>
                    <span>67%</span>
                </div>
                <div class="language-bar">
                    <div class="language-fill" style="width: 67%;"></div>
                </div>
            </div>

            <div class="language-item">
                <div class="language-name">
                    <span>JSX/TSX</span>
                    <span>18%</span>
                </div>
                <div class="language-bar">
                    <div class="language-fill" style="width: 18%;"></div>
                </div>
            </div>

            <div class="language-item">
                <div class="language-name">
                    <span>CSS</span>
                    <span>10%</span>
                </div>
                <div class="language-bar">
                    <div class="language-fill" style="width: 10%;"></div>
                </div>
            </div>

            <div class="language-item">
                <div class="language-name">
                    <span>HTML</span>
                    <span>5%</span>
                </div>
                <div class="language-bar">
                    <div class="language-fill" style="width: 5%;"></div>
                </div>
            </div>
        </div>

        <!-- Contributions Calendar -->
        <div class="contributions">
            <h3>Contributions Calendar</h3>
            <div class="calendar-grid">
                <div class="calendar-day"></div>
                <div class="calendar-day active-1"></div>
                <div class="calendar-day active-2"></div>
                <div class="calendar-day active-3"></div>
                <div class="calendar-day active-2"></div>
                <div class="calendar-day active-1"></div>
                <div class="calendar-day"></div>
                <div class="calendar-day active-1"></div>
                <div class="calendar-day active-2"></div>
                <div class="calendar-day active-3"></div>
                <div class="calendar-day active-2"></div>
                <div class="calendar-day active-1"></div>
                <div class="calendar-day"></div>
                <div class="calendar-day active-1"></div>
                <div class="calendar-day active-2"></div>
                <div class="calendar-day active-3"></div>
                <div class="calendar-day active-2"></div>
                <div class="calendar-day active-1"></div>
                <div class="calendar-day"></div>
                <div class="calendar-day"></div>
                <div class="calendar-day active-1"></div>
                <div class="calendar-day active-2"></div>
                <div class="calendar-day active-1"></div>
                <div class="calendar-day"></div>
                <div class="calendar-day active-1"></div>
                <div class="calendar-day active-3"></div>
                <div class="calendar-day active-2"></div>
                <div class="calendar-day active-1"></div>
                <div class="calendar-day"></div>
                <div class="calendar-day active-1"></div>
                <div class="calendar-day active-2"></div>
                <div class="calendar-day active-3"></div>
                <div class="calendar-day active-2"></div>
                <div class="calendar-day active-1"></div>
                <div class="calendar-day"></div>
                <div class="calendar-day active-1"></div>
                <div class="calendar-day active-2"></div>
                <div class="calendar-day active-1"></div>
            </div>
            <p style="color: #8b949e; font-size: 0.9rem;">Current streak: <strong style="color: #00ff41;">2 days</strong> | ~3.82 commits per day</p>
        </div>

        <!-- Projects Section -->
        <div class="projects">
            <h3>Featured Projects</h3>
            <div class="projects-grid">
                <div class="project-card">
                    <h4>Project Roadmap & Todos</h4>
                    <p>Updated less than 1 day ago</p>
                    <p style="margin-top: 10px;">19 Done · 1 Doing · 8 Todo</p>
                </div>

                <div class="project-card">
                    <h4>Interactive React Components</h4>
                    <p>High-performance reusable components</p>
                    <p style="margin-top: 10px;">Built with React, TypeScript & Tailwind CSS</p>
                </div>

                <div class="project-card">
                    <h4>Next.js Full-Stack Apps</h4>
                    <p>Production-ready applications</p>
                    <p style="margin-top: 10px;">REST APIs, Database Integration & Authentication</p>
                </div>
            </div>
        </div>

        <!-- Footer -->
        <footer>
            <p style="margin-bottom: 20px;">© 2025 Gulshan Kumar • Frontend Developer from Lucknow, India</p>
            <div class="social-links">
                <a href="#">GitHub</a>
                <a href="#">LinkedIn</a>
                <a href="#">Twitter</a>
                <a href="#">Portfolio</a>
            </div>
        </footer>
    </div>
</body>
</html>
