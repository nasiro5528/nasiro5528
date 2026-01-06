<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nasir Mohammed | Developer Portfolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Roboto+Mono:wght@300;400;500&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary-color: #2d5af1;
            --secondary-color: #6c63ff;
            --accent-color: #ff6b8b;
            --dark-color: #121826;
            --light-color: #f8f9fa;
            --gray-color: #6c757d;
            --success-color: #28a745;
            --card-bg: rgba(255, 255, 255, 0.05);
            --border-radius: 12px;
            --box-shadow: 0 8px 30px rgba(0, 0, 0, 0.12);
            --transition: all 0.3s ease;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #0f172a, #1e293b);
            color: var(--light-color);
            line-height: 1.6;
            overflow-x: hidden;
            padding: 20px;
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Header & Hero Section */
        .hero-section {
            text-align: center;
            padding: 40px 20px;
            margin-bottom: 40px;
            position: relative;
            overflow: hidden;
            border-radius: var(--border-radius);
            background: linear-gradient(135deg, rgba(45, 90, 241, 0.1), rgba(108, 99, 255, 0.1));
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .profile-pic {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            margin: 0 auto 20px;
            overflow: hidden;
            border: 4px solid var(--primary-color);
            position: relative;
            animation: float 6s ease-in-out infinite;
            box-shadow: 0 0 30px rgba(45, 90, 241, 0.4);
        }

        .profile-pic::before {
            content: '';
            position: absolute;
            top: -10px;
            left: -10px;
            right: -10px;
            bottom: -10px;
            background: linear-gradient(45deg, var(--primary-color), var(--secondary-color), var(--accent-color));
            border-radius: 50%;
            z-index: -1;
            animation: rotate 10s linear infinite;
        }

        .profile-pic img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 50%;
            background-color: #1a2332;
            padding: 5px;
        }

        .hero-content h1 {
            font-size: 2.8rem;
            margin-bottom: 10px;
            background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        .tagline {
            font-size: 1.3rem;
            color: #cbd5e1;
            margin-bottom: 20px;
            font-weight: 300;
        }

        .highlight {
            color: var(--accent-color);
            font-weight: 600;
        }

        /* Section Styles */
        .section {
            background: var(--card-bg);
            backdrop-filter: blur(10px);
            border-radius: var(--border-radius);
            padding: 30px;
            margin-bottom: 30px;
            border: 1px solid rgba(255, 255, 255, 0.05);
            transition: var(--transition);
            box-shadow: var(--box-shadow);
        }

        .section:hover {
            transform: translateY(-5px);
            box-shadow: 0 12px 40px rgba(0, 0, 0, 0.2);
        }

        .section-title {
            display: flex;
            align-items: center;
            margin-bottom: 25px;
            color: var(--light-color);
            font-size: 1.5rem;
        }

        .section-title i {
            margin-right: 15px;
            color: var(--primary-color);
            font-size: 1.8rem;
        }

        /* Skills Grid */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .skill-category {
            background: rgba(255, 255, 255, 0.03);
            border-radius: var(--border-radius);
            padding: 20px;
            transition: var(--transition);
        }

        .skill-category:hover {
            background: rgba(255, 255, 255, 0.07);
            transform: translateY(-3px);
        }

        .skill-category h3 {
            color: var(--primary-color);
            margin-bottom: 15px;
            font-size: 1.2rem;
            display: flex;
            align-items: center;
        }

        .skill-category h3 i {
            margin-right: 10px;
        }

        .skill-list {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }

        .skill-item {
            background: rgba(45, 90, 241, 0.15);
            padding: 8px 15px;
            border-radius: 50px;
            font-size: 0.9rem;
            transition: var(--transition);
            border: 1px solid rgba(45, 90, 241, 0.2);
        }

        .skill-item:hover {
            background: rgba(45, 90, 241, 0.3);
            transform: scale(1.05);
        }

        /* Projects Grid */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 25px;
            margin-top: 20px;
        }

        .project-card {
            background: rgba(255, 255, 255, 0.03);
            border-radius: var(--border-radius);
            overflow: hidden;
            transition: var(--transition);
            border: 1px solid rgba(255, 255, 255, 0.05);
        }

        .project-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.2);
        }

        .project-header {
            padding: 20px;
            background: rgba(45, 90, 241, 0.1);
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
        }

        .project-header h3 {
            color: var(--light-color);
            margin-bottom: 5px;
        }

        .project-tech {
            font-size: 0.85rem;
            color: var(--gray-color);
        }

        .project-body {
            padding: 20px;
        }

        .project-link {
            display: inline-block;
            margin-top: 15px;
            color: var(--primary-color);
            text-decoration: none;
            font-weight: 500;
            transition: var(--transition);
        }

        .project-link:hover {
            color: var(--accent-color);
        }

        /* Contact Section */
        .contact-links {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 20px;
        }

        .contact-link {
            display: flex;
            align-items: center;
            background: rgba(255, 255, 255, 0.05);
            padding: 15px 25px;
            border-radius: var(--border-radius);
            text-decoration: none;
            color: var(--light-color);
            transition: var(--transition);
            border: 1px solid rgba(255, 255, 255, 0.05);
        }

        .contact-link:hover {
            background: rgba(45, 90, 241, 0.2);
            transform: translateY(-3px);
            border-color: var(--primary-color);
        }

        .contact-link i {
            margin-right: 10px;
            font-size: 1.3rem;
            color: var(--primary-color);
        }

        /* Animations */
        @keyframes float {
            0%, 100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-15px);
            }
        }

        @keyframes rotate {
            0% {
                transform: rotate(0deg);
            }
            100% {
                transform: rotate(360deg);
            }
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .fade-in {
            animation: fadeIn 0.8s ease forwards;
        }

        .delay-1 {
            animation-delay: 0.2s;
        }

        .delay-2 {
            animation-delay: 0.4s;
        }

        .delay-3 {
            animation-delay: 0.6s;
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 30px 0;
            color: var(--gray-color);
            font-size: 0.9rem;
            border-top: 1px solid rgba(255, 255, 255, 0.05);
            margin-top: 30px;
        }

        .pulse {
            display: inline-block;
            width: 10px;
            height: 10px;
            background-color: var(--success-color);
            border-radius: 50%;
            margin-right: 8px;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% {
                transform: scale(0.9);
                box-shadow: 0 0 0 0 rgba(40, 167, 69, 0.7);
            }
            70% {
                transform: scale(1);
                box-shadow: 0 0 0 10px rgba(40, 167, 69, 0);
            }
            100% {
                transform: scale(0.9);
                box-shadow: 0 0 0 0 rgba(40, 167, 69, 0);
            }
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .hero-content h1 {
                font-size: 2.2rem;
            }
            
            .section {
                padding: 20px;
            }
            
            .skills-grid, .projects-grid {
                grid-template-columns: 1fr;
            }
            
            .contact-links {
                flex-direction: column;
            }
            
            .contact-link {
                justify-content: center;
            }
        }

        @media (max-width: 480px) {
            .hero-content h1 {
                font-size: 1.8rem;
            }
            
            .tagline {
                font-size: 1.1rem;
            }
            
            .section-title {
                font-size: 1.3rem;
            }
            
            .profile-pic {
                width: 120px;
                height: 120px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Hero Section -->
        <section class="hero-section fade-in">
            <div class="profile-pic">
                <img src="https://avatars.githubusercontent.com/u/placeholder" alt="Nasir Mohammed">
            </div>
            <div class="hero-content">
                <h1>Nasir Mohammed</h1>
                <p class="tagline">Passionate Developer & Technology Enthusiast</p>
                <p>Dedicated to crafting innovative solutions that drive success. I blend technology with creativity to deliver exceptional results.</p>
                <div style="margin-top: 20px;">
                    <span class="pulse"></span>
                    <span>Available for collaborations</span>
                </div>
            </div>
        </section>

        <!-- Skills Section -->
        <section class="section fade-in delay-1">
            <div class="section-title">
                <i class="fas fa-code"></i>
                <h2>Technologies & Tools</h2>
            </div>
            <div class="skills-grid">
                <div class="skill-category">
                    <h3><i class="fas fa-laptop-code"></i> Programming Languages</h3>
                    <div class="skill-list">
                        <span class="skill-item">JavaScript</span>
                        <span class="skill-item">Python</span>
                        <span class="skill-item">TypeScript</span>
                        <span class="skill-item">C++</span>
                        <span class="skill-item">C#</span>
                        <span class="skill-item">R</span>
                        <span class="skill-item">HTML/CSS</span>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3><i class="fas fa-layer-group"></i> Frameworks & Tools</h3>
                    <div class="skill-list">
                        <span class="skill-item">React</span>
                        <span class="skill-item">Next.js</span>
                        <span class="skill-item">Node.js</span>
                        <span class="skill-item">Git</span>
                        <span class="skill-item">Docker</span>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3><i class="fas fa-network-wired"></i> Networking</h3>
                    <div class="skill-list">
                        <span class="skill-item">Cisco Networking</span>
                        <span class="skill-item">AWS</span>
                        <span class="skill-item">GCP</span>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3><i class="fas fa-paint-brush"></i> Design</h3>
                    <div class="skill-list">
                        <span class="skill-item">UI/UX Design</span>
                        <span class="skill-item">Adobe Premiere</span>
                        <span class="skill-item">Final Cut Pro</span>
                        <span class="skill-item">Power BI</span>
                    </div>
                </div>
            </div>
        </section>

        <!-- Currently Learning Section -->
        <section class="section fade-in delay-2">
            <div class="section-title">
                <i class="fas fa-graduation-cap"></i>
                <h2>Currently Learning</h2>
            </div>
            <div class="skills-grid">
                <div class="skill-category">
                    <h3><i class="fas fa-brain"></i> Machine Learning</h3>
                    <p>Exploring algorithms and predictive analytics</p>
                </div>
                
                <div class="skill-category">
                    <h3><i class="fas fa-user-circle"></i> Advanced UI/UX Design</h3>
                    <p>Diving deeper into user-centered design methodologies</p>
                </div>
                
                <div class="skill-category">
                    <h3><i class="fas fa-chart-bar"></i> Data Visualization</h3>
                    <p>Enhancing abilities in data storytelling through visualization tools</p>
                </div>
            </div>
        </section>

        <!-- Projects Section -->
        <section class="section fade-in delay-1">
            <div class="section-title">
                <i class="fas fa-rocket"></i>
                <h2>Notable Projects</h2>
            </div>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-header">
                        <h3>Employee Task Management System</h3>
                        <div class="project-tech">React, Node.js, MongoDB</div>
                    </div>
                    <div class="project-body">
                        <p>A cutting-edge application designed to streamline task management and enhance team collaboration.</p>
                        <a href="#" class="project-link">View Project <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-header">
                        <h3>Resident Record System</h3>
                        <div class="project-tech">MySQL, PHP, JavaScript</div>
                    </div>
                    <div class="project-body">
                        <p>A comprehensive Resident Record System showcasing database management and web development skills.</p>
                        <a href="https://github.com/nasir5528/resident-record-system" class="project-link">View on GitHub <i class="fas fa-external-link-alt"></i></a>
                    </div>
                </div>
            </div>
        </section>

        <!-- Contact Section -->
        <section class="section fade-in delay-2">
            <div class="section-title">
                <i class="fas fa-paper-plane"></i>
                <h2>Let's Connect!</h2>
            </div>
            <p style="margin-bottom: 20px;">I believe in the power of collaboration and would love to connect with fellow professionals.</p>
            <div class="contact-links">
                <a href="mailto:warenasir749@gmail.com" class="contact-link">
                    <i class="fas fa-envelope"></i>
                    <span>warenasir749@gmail.com</span>
                </a>
                
                <a href="https://linkedin.com/in/nasirmohammed" class="contact-link">
                    <i class="fab fa-linkedin"></i>
                    <span>Connect on LinkedIn</span>
                </a>
                
                <a href="https://github.com/nasir5528" class="contact-link">
                    <i class="fab fa-github"></i>
                    <span>GitHub Profile</span>
                </a>
            </div>
        </section>

        <footer>
            <p>© 2023 Nasir Mohammed. All rights reserved.</p>
            <p style="margin-top: 10px; font-size: 0.8rem;">Crafted with <i class="fas fa-heart" style="color: var(--accent-color);"></i> and code</p>
        </footer>
    </div>

    <script>
        // Add scroll animation for sections
        document.addEventListener('DOMContentLoaded', function() {
            const fadeElements = document.querySelectorAll('.fade-in');
            
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('animated');
                    }
                });
            }, {
                threshold: 0.1
            });
            
            fadeElements.forEach(el => observer.observe(el));
            
            // Add hover effect to project cards
            const projectCards = document.querySelectorAll('.project-card');
            projectCards.forEach(card => {
                card.addEventListener('mouseenter', function() {
                    this.style.transform = 'translateY(-8px)';
                });
                
                card.addEventListener('mouseleave', function() {
                    this.style.transform = 'translateY(0)';
                });
            });
            
            // Animate skill items on hover
            const skillItems = document.querySelectorAll('.skill-item');
            skillItems.forEach(item => {
                item.addEventListener('mouseenter', function() {
                    this.style.transform = 'scale(1.05)';
                });
                
                item.addEventListener('mouseleave', function() {
                    this.style.transform = 'scale(1)';
                });
            });
        });
    </script>
</body>
</html>
