<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Khalid Majid Shaikh - Full-Stack Developer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #0f0f1e 0%, #1a1a2e 50%, #0f0f1e 100%);
            color: #e0e0e0;
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 40px 20px;
        }

        /* Hero Section */
        .hero {
            text-align: center;
            padding: 60px 20px;
            background: linear-gradient(135deg, rgba(100, 200, 255, 0.1) 0%, rgba(100, 150, 255, 0.05) 100%);
            border-radius: 20px;
            border: 1px solid rgba(100, 200, 255, 0.2);
            margin-bottom: 60px;
            animation: slideDown 0.6s ease-out;
        }

        @keyframes slideDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .hero h1 {
            font-size: 3.5em;
            color: #64c8ff;
            margin-bottom: 10px;
            font-weight: 700;
            text-shadow: 0 0 20px rgba(100, 200, 255, 0.3);
        }

        .hero .subtitle {
            font-size: 1.5em;
            color: #a0c8ff;
            margin-bottom: 10px;
            font-weight: 300;
        }

        .hero .tagline {
            font-size: 1.1em;
            color: #888;
            margin-bottom: 30px;
        }

        .badge-container {
            display: flex;
            gap: 15px;
            justify-content: center;
            flex-wrap: wrap;
            margin-top: 30px;
        }

        .badge {
            display: inline-block;
            padding: 10px 20px;
            background: linear-gradient(135deg, #64c8ff 0%, #6ca8ff 100%);
            color: #000;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
        }

        .badge:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(100, 200, 255, 0.4);
        }

        /* Section Headers */
        .section-header {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 40px;
            padding-bottom: 20px;
            border-bottom: 2px solid rgba(100, 200, 255, 0.3);
        }

        .section-header h2 {
            font-size: 2.2em;
            color: #64c8ff;
            font-weight: 700;
        }

        .section-header .emoji {
            font-size: 2.5em;
        }

        /* About Section */
        .about {
            background: rgba(30, 30, 50, 0.5);
            padding: 40px;
            border-radius: 15px;
            border: 1px solid rgba(100, 200, 255, 0.15);
            margin-bottom: 60px;
            backdrop-filter: blur(10px);
        }

        .about p {
            font-size: 1.1em;
            margin-bottom: 20px;
            color: #ccc;
            line-height: 1.8;
        }

        .about ul {
            list-style: none;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin-top: 20px;
        }

        .about li {
            padding: 15px;
            background: rgba(100, 200, 255, 0.05);
            border-left: 3px solid #64c8ff;
            border-radius: 5px;
            transition: all 0.3s ease;
        }

        .about li:hover {
            background: rgba(100, 200, 255, 0.1);
            transform: translateX(5px);
        }

        /* Tech Stack */
        .tech-section {
            margin-bottom: 60px;
        }

        .tech-categories {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }

        .tech-category {
            background: rgba(30, 30, 50, 0.5);
            padding: 30px;
            border-radius: 15px;
            border: 1px solid rgba(100, 200, 255, 0.15);
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
        }

        .tech-category:hover {
            border-color: rgba(100, 200, 255, 0.4);
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(100, 200, 255, 0.2);
        }

        .tech-category h3 {
            color: #64c8ff;
            font-size: 1.4em;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .tech-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 12px;
        }

        .tech-item {
            padding: 12px 15px;
            background: rgba(100, 200, 255, 0.1);
            border: 1px solid rgba(100, 200, 255, 0.2);
            border-radius: 8px;
            text-align: center;
            font-size: 0.95em;
            transition: all 0.3s ease;
            font-weight: 500;
        }

        .tech-item:hover {
            background: rgba(100, 200, 255, 0.2);
            border-color: #64c8ff;
            color: #64c8ff;
        }

        /* Portfolio Section */
        .portfolio {
            background: rgba(30, 30, 50, 0.5);
            padding: 40px;
            border-radius: 15px;
            border: 1px solid rgba(100, 200, 255, 0.15);
            margin-bottom: 60px;
            backdrop-filter: blur(10px);
        }

        .portfolio h3 {
            color: #64c8ff;
            font-size: 1.3em;
            margin-bottom: 15px;
        }

        .portfolio p {
            color: #ccc;
            margin-bottom: 15px;
            line-height: 1.8;
        }

        .portfolio-link {
            display: inline-block;
            padding: 12px 25px;
            background: linear-gradient(135deg, #64c8ff 0%, #6ca8ff 100%);
            color: #000;
            border-radius: 8px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            margin-top: 15px;
        }

        .portfolio-link:hover {
            transform: translateX(5px);
            box-shadow: 0 10px 25px rgba(100, 200, 255, 0.3);
        }

        .portfolio-features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }

        .feature {
            padding: 15px;
            background: rgba(100, 200, 255, 0.05);
            border-radius: 8px;
            border-left: 3px solid #64c8ff;
        }

        .feature strong {
            color: #64c8ff;
        }

        /* Projects Section */
        .projects {
            background: rgba(30, 30, 50, 0.5);
            padding: 40px;
            border-radius: 15px;
            border: 1px solid rgba(100, 200, 255, 0.15);
            margin-bottom: 60px;
            backdrop-filter: blur(10px);
            text-align: center;
        }

        .projects p {
            color: #ccc;
            margin-bottom: 25px;
            font-size: 1.1em;
            line-height: 1.8;
        }

        /* Stats Section */
        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-bottom: 60px;
        }

        .stat-card {
            background: rgba(30, 30, 50, 0.5);
            padding: 30px;
            border-radius: 15px;
            border: 1px solid rgba(100, 200, 255, 0.15);
            text-align: center;
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
        }

        .stat-card:hover {
            border-color: rgba(100, 200, 255, 0.4);
            transform: translateY(-5px);
        }

        .stat-card .number {
            font-size: 2.5em;
            color: #64c8ff;
            font-weight: 700;
            margin-bottom: 10px;
        }

        .stat-card .label {
            color: #888;
            font-size: 0.95em;
        }

        /* Contact Section */
        .contact {
            background: linear-gradient(135deg, rgba(100, 200, 255, 0.1) 0%, rgba(100, 150, 255, 0.05) 100%);
            padding: 50px 40px;
            border-radius: 15px;
            border: 1px solid rgba(100, 200, 255, 0.2);
            text-align: center;
            margin-bottom: 40px;
        }

        .contact h2 {
            color: #64c8ff;
            font-size: 2em;
            margin-bottom: 30px;
        }

        .contact-links {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .contact-link {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            padding: 12px 25px;
            background: rgba(100, 200, 255, 0.1);
            border: 1px solid rgba(100, 200, 255, 0.3);
            border-radius: 50px;
            color: #64c8ff;
            text-decoration: none;
            transition: all 0.3s ease;
            font-weight: 500;
        }

        .contact-link:hover {
            background: rgba(100, 200, 255, 0.2);
            border-color: #64c8ff;
            transform: translateY(-3px);
        }

        /* Footer */
        .footer {
            text-align: center;
            padding: 30px;
            color: #666;
            border-top: 1px solid rgba(100, 200, 255, 0.1);
        }

        .footer p {
            margin-bottom: 10px;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5em;
            }

            .hero .subtitle {
                font-size: 1.2em;
            }

            .about ul {
                grid-template-columns: 1fr;
            }

            .badge-container {
                flex-direction: column;
            }

            .badge {
                width: 100%;
                text-align: center;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Hero Section -->
        <div class="hero">
            <h1>Hi, I'm Khalid Majid Shaikh</h1>
            <div class="subtitle">Full-Stack Developer & DevOps Architect</div>
            <p class="tagline">Building scalable web applications with cutting-edge technologies | Based in India</p>
            <div class="badge-container">
                <a href="https://khalid7.vercel.app/" class="badge" target="_blank">Portfolio</a>
                <a href="https://www.linkedin.com/in/shaikhkhalid007/" class="badge" target="_blank">LinkedIn</a>
                <a href="mailto:ks0903525@gmail.com" class="badge">Email</a>
            </div>
        </div>

        <!-- About Section -->
        <div class="about">
            <div class="section-header">
                <span class="emoji">●</span>
                <h2>About Me</h2>
            </div>
            <p>
                I'm a passionate full-stack developer with a <strong>Bachelor's degree in IT</strong> from Vidya Vikas College (University of Mumbai). I specialize in building modern, scalable web applications using cutting-edge technologies. My journey in development is driven by curiosity, creativity, and a commitment to writing clean, maintainable code.
            </p>
            <ul>
                <li><strong>Full-Stack Developer</strong> with expertise across the entire stack</li>
                <li><strong>Problem Solver</strong> who loves building intuitive user experiences</li>
                <li><strong>DevOps & Cloud</strong> focused on scalable deployments</li>
                <li><strong>Continuous Learner</strong> staying updated with latest trends</li>
                <li><strong>Mobile Development</strong> with React Native & Kotlin</li>
                <li><strong>Backend Architecture</strong> designing robust systems</li>
            </ul>
        </div>

        <!-- Tech Stack Section -->
        <div class="tech-section">
            <div class="section-header">
                <span class="emoji">▲</span>
                <h2>Tech Stack</h2>
            </div>
            <div class="tech-categories">
                <div class="tech-category">
                    <h3>Frontend</h3>
                    <div class="tech-grid">
                        <div class="tech-item">HTML5</div>
                        <div class="tech-item">CSS3</div>
                        <div class="tech-item">JavaScript</div>
                        <div class="tech-item">React</div>
                        <div class="tech-item">Tailwind CSS</div>
                        <div class="tech-item">Responsive Design</div>
                    </div>
                </div>

                <div class="tech-category">
                    <h3>Backend & Mobile</h3>
                    <div class="tech-grid">
                        <div class="tech-item">Node.js</div>
                        <div class="tech-item">Express.js</div>
                        <div class="tech-item">C#</div>
                        <div class="tech-item">Kotlin</div>
                        <div class="tech-item">React Native</div>
                        <div class="tech-item">REST APIs</div>
                    </div>
                </div>

                <div class="tech-category">
                    <h3>Database & Tools</h3>
                    <div class="tech-grid">
                        <div class="tech-item">MongoDB</div>
                        <div class="tech-item">MySQL</div>
                        <div class="tech-item">Git & GitHub</div>
                        <div class="tech-item">Docker</div>
                        <div class="tech-item">Vercel</div>
                        <div class="tech-item">DevOps</div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Portfolio Section -->
        <div class="portfolio">
            <div class="section-header">
                <span class="emoji">💼</span>
                <h2>My Portfolio Website</h2>
            </div>
            <p>
                I've built a modern, responsive portfolio website showcasing my projects and skills with a clean design, smooth animations, and optimal performance.
            </p>
            <div class="portfolio-features">
                <div class="feature">
                    <strong>Frontend:</strong> React, Tailwind CSS, HTML5
                </div>
                <div class="feature">
                    <strong>Deployment:</strong> Vercel & GitHub Pages
                </div>
                <div class="feature">
                    <strong>Features:</strong> Fully Responsive, Modern UI
                </div>
                <div class="feature">
                    <strong>Experience:</strong> Smooth Animations & Fast Loading
                </div>
            </div>
            <a href="https://khalid7.vercel.app/" class="portfolio-link" target="_blank">→ Visit My Portfolio</a>
        </div>

        <!-- Projects Section -->
        <div class="projects">
            <div class="section-header">
                <span class="emoji">🚀</span>
                <h2>Featured Projects</h2>
            </div>
            <p>
                I regularly build full-stack applications and contribute to open-source projects. Explore my repositories to see innovative solutions and well-structured code. Each project demonstrates my commitment to quality and modern development practices.
            </p>
            <a href="https://khalid7.vercel.app/" class="portfolio-link" target="_blank">View All Projects</a>
        </div>

        <!-- Contact Section -->
        <div class="contact">
            <h2>🤝 Let's Connect & Collaborate</h2>
            <p style="color: #aaa; margin-bottom: 25px;">I'm always excited to work on challenging projects and connect with fellow developers!</p>
            <div class="contact-links">
                <a href="mailto:ks0903525@gmail.com" class="contact-link">📧 Email Me</a>
                <a href="https://www.linkedin.com/in/shaikhkhalid007/" class="contact-link" target="_blank">💼 LinkedIn</a>
                <a href="https://khalid7.vercel.app/" class="contact-link" target="_blank">🌐 Portfolio</a>
                <a href="https://github.com/k-halid007" class="contact-link" target="_blank">💻 GitHub</a>
            </div>
        </div>

        <!-- Footer -->
        <div class="footer">
            <p>💜 Made with passion by Khalid Majid Shaikh</p>
            <p>© 2024 | Full-Stack Developer | India</p>
        </div>
    </div>
</body>
</html>
