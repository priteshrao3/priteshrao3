<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pritesh Prasad - Full Stack Developer</title>
    <style>
        :root {
            --primary-color: #2d4b8e;
            --secondary-color: #47b475;
            --accent-color: #ff6b6b;
            --light-color: #f8f9fa;
            --dark-color: #343a40;
            --text-color: #333;
            --transition: all 0.3s ease;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: var(--text-color);
            background-color: #f5f7f9;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        header {
            background: linear-gradient(135deg, var(--primary-color), #1e3261);
            color: white;
            padding: 60px 0;
            text-align: center;
        }
        
        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 5px solid rgba(255, 255, 255, 0.3);
            margin-bottom: 20px;
            object-fit: cover;
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }
        
        .tagline {
            font-size: 1.2rem;
            opacity: 0.9;
            margin-bottom: 20px;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-link {
            color: white;
            text-decoration: none;
            padding: 8px 15px;
            border-radius: 4px;
            background-color: rgba(255, 255, 255, 0.2);
            transition: var(--transition);
        }
        
        .social-link:hover {
            background-color: rgba(255, 255, 255, 0.3);
            transform: translateY(-2px);
        }
        
        section {
            padding: 60px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 40px;
            color: var(--primary-color);
            position: relative;
        }
        
        .section-title::after {
            content: '';
            display: block;
            width: 60px;
            height: 3px;
            background-color: var(--secondary-color);
            margin: 10px auto;
        }
        
        .summary {
            background-color: white;
            border-radius: 8px;
            padding: 30px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            margin-bottom: 30px;
        }
        
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
        }
        
        .skill-category {
            background-color: white;
            border-radius: 8px;
            padding: 20px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .skill-category h3 {
            color: var(--primary-color);
            margin-bottom: 15px;
            padding-bottom: 10px;
            border-bottom: 1px solid #eee;
        }
        
        .skill-list {
            list-style-type: none;
        }
        
        .skill-list li {
            padding: 8px 0;
            border-bottom: 1px solid #f5f5f5;
            display: flex;
            align-items: center;
        }
        
        .skill-list li:before {
            content: "▹";
            color: var(--secondary-color);
            margin-right: 10px;
        }
        
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 25px;
        }
        
        .project-card {
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: var(--transition);
        }
        
        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
        }
        
        .project-content {
            padding: 20px;
        }
        
        .project-title {
            color: var(--primary-color);
            margin-bottom: 10px;
        }
        
        .project-description {
            margin-bottom: 15px;
            font-size: 0.95rem;
        }
        
        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-bottom: 15px;
        }
        
        .tech-tag {
            background-color: #e9ecef;
            color: var(--dark-color);
            padding: 4px 10px;
            border-radius: 20px;
            font-size: 0.8rem;
        }
        
        .project-link {
            display: inline-block;
            color: var(--secondary-color);
            text-decoration: none;
            font-weight: 500;
            transition: var(--transition);
        }
        
        .project-link:hover {
            color: var(--primary-color);
        }
        
        .experience-item {
            background-color: white;
            border-radius: 8px;
            padding: 25px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            margin-bottom: 20px;
        }
        
        .experience-header {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            margin-bottom: 15px;
        }
        
        .company {
            font-weight: bold;
            color: var(--primary-color);
        }
        
        .date {
            color: #6c757d;
            font-size: 0.9rem;
        }
        
        .position {
            font-style: italic;
            margin-bottom: 10px;
        }
        
        footer {
            background-color: var(--dark-color);
            color: white;
            text-align: center;
            padding: 30px 0;
        }
        
        @media (max-width: 768px) {
            .skills-grid, .projects-grid {
                grid-template-columns: 1fr;
            }
            
            .experience-header {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <!-- Placeholder for profile image - replace with actual image URL -->
            <img src="https://via.placeholder.com/150" alt="Pritesh Prasad" class="profile-img">
            <h1>Pritesh Prasad</h1>
            <p class="tagline">Full Stack Developer | Django | Next.js | Flutter | DevOps</p>
            <div class="social-links">
                <a href="https://wa.me/message/IPNAQPOXX6FJO1?src=qr" class="social-link">WhatsApp</a>
                <a href="https://www.linkedin.com/in/pritesh-prasad-242390176" class="social-link">LinkedIn</a>
                <a href="https://www.facebook.com/share/DqLkTchZWGeffQP6/" class="social-link">Facebook</a>
                <a href="mailto:priteshrao3@gmail.com" class="social-link">Email</a>
            </div>
        </div>
    </header>

    <section id="about">
        <div class="container">
            <h2 class="section-title">About Me</h2>
            <div class="summary">
                <p>Experienced Full Stack Developer with over 3+ years of experience in designing, developing, and deploying scalable web and mobile applications. Proficient in both frontend and backend development with strong command over Python, Django, Next.js, Flutter, and RESTful APIs. Skilled in cloud deployments, containerization, and performance optimization. Passionate about creating clean, maintainable code and user-centric digital solutions.</p>
            </div>
        </div>
    </section>

    <section id="skills">
        <div class="container">
            <h2 class="section-title">Technical Skills</h2>
            <div class="skills-grid">
                <div class="skill-category">
                    <h3>Languages & Frameworks</h3>
                    <ul class="skill-list">
                        <li>Python</li>
                        <li>JavaScript</li>
                        <li>Dart</li>
                        <li>HTML/CSS</li>
                        <li>Django</li>
                        <li>Django REST Framework</li>
                        <li>FastAPI</li>
                        <li>Next.js</li>
                        <li>Flutter</li>
                        <li>Bootstrap</li>
                        <li>Tailwind CSS</li>
                        <li>Ant Design</li>
                        <li>GraphQL</li>
                    </ul>
                </div>
                
                <div class="skill-category">
                    <h3>Mobile Development</h3>
                    <ul class="skill-list">
                        <li>Flutter (Cross-platform)</li>
                        <li>Firebase Integration</li>
                        <li>State Management (GetX)</li>
                    </ul>
                    
                    <h3>Backend & API</h3>
                    <ul class="skill-list">
                        <li>REST APIs</li>
                        <li>GraphQL</li>
                        <li>WebSockets</li>
                        <li>JWT/OAuth Authentication</li>
                        <li>Celery</li>
                        <li>Redis Queue</li>
                    </ul>
                </div>
                
                <div class="skill-category">
                    <h3>Databases</h3>
                    <ul class="skill-list">
                        <li>MySQL</li>
                        <li>PostgreSQL</li>
                        <li>MongoDB</li>
                        <li>SQLite</li>
                        <li>Redis</li>
                    </ul>
                    
                    <h3>DevOps & Cloud</h3>
                    <ul class="skill-list">
                        <li>Docker</li>
                        <li>Kubernetes</li>
                        <li>AWS (EC2, S3)</li>
                        <li>Azure</li>
                        <li>Google Cloud</li>
                        <li>DigitalOcean</li>
                        <li>Vercel</li>
                        <li>PythonAnywhere</li>
                        <li>VPS Hosting</li>
                        <li>Nginx</li>
                    </ul>
                </div>
                
                <div class="skill-category">
                    <h3>Tools & Technologies</h3>
                    <ul class="skill-list">
                        <li>Git, GitHub, GitLab</li>
                        <li>GitHub Actions</li>
                        <li>Linux (Ubuntu, Kali)</li>
                        <li>Bash/Shell Scripting</li>
                        <li>Selenium</li>
                        <li>Postman</li>
                        <li>Swagger</li>
                        <li>Alembic</li>
                        <li>Sentry</li>
                        <li>Google Docs API</li>
                        <li>OpenAI/ChatGPT API</li>
                        <li>Apache Kafka</li>
                        <li>RabbitMQ</li>
                        <li>Zookeeper</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <section id="experience">
        <div class="container">
            <h2 class="section-title">Professional Experience</h2>
            
            <div class="experience-item">
                <div class="experience-header">
                    <span class="company">BK Arogyam Pvt. Ltd., Varanasi</span>
                    <span class="date">Oct 2022 – Present</span>
                </div>
                <div class="position">Full Stack Developer</div>
                <ul class="skill-list">
                    <li>Led development of scalable web applications and ERP systems tailored for the healthcare domain</li>
                    <li>Created dynamic frontend interfaces with Next.js, Tailwind CSS, and integrated with Django/FastAPI backends</li>
                    <li>Built and maintained RESTful APIs and asynchronous services using Celery and Redis</li>
                    <li>Implemented authentication systems, role-based access control, and data security practices</li>
                    <li>Managed Docker-based deployment, Nginx configuration, and cloud hosting on AWS and DigitalOcean</li>
                    <li>Collaborated on the development and deployment of multiple Flutter-based mobile apps</li>
                </ul>
            </div>
            
            <div class="experience-item">
                <div class="experience-header">
                    <span class="company">Techavera Solutions Pvt. Ltd., Noida</span>
                    <span class="date">May 2022 – July 2022</span>
                </div>
                <div class="position">Python Web Developer Intern</div>
                <ul class="skill-list">
                    <li>Built Django web applications with authentication and database integration</li>
                    <li>Worked on CRUD-based modules, admin customizations, and deployment procedures</li>
                    <li>Gained foundational experience in REST API development and Django architecture</li>
                </ul>
            </div>
            
            <div class="experience-item">
                <div class="experience-header">
                    <span class="company">SVS Tech Online</span>
                    <span class="date">2018 – 2021</span>
                </div>
                <div class="position">Email Marketing Specialist</div>
                <ul class="skill-list">
                    <li>4 years of experience in email marketing campaigns and strategies</li>
                </ul>
            </div>
        </div>
    </section>

    <section id="projects">
        <div class="container">
            <h2 class="section-title">Projects</h2>
            <div class="projects-grid">
                
                <div class="project-card">
                    <div class="project-content">
                        <h3 class="project-title">BK Arogyam</h3>
                        <p class="project-description">Developed and maintained the website for B.K. Arogyam, a renowned Kidney Ayurvedic hospital using Django framework.</p>
                        <div class="project-tech">
                            <span class="tech-tag">Django</span>
                            <span class="tech-tag">PostgreSQL</span>
                            <span class="tech-tag">JavaScript</span>
                            <span class="tech-tag">Bootstrap</span>
                        </div>
                        <a href="https://www.bkarogyam.com/" class="project-link">View Project</a>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-content">
                        <h3 class="project-title">Arogya Bharat</h3>
                        <p class="project-description">Medical professionals portal for doctors and advisors with doctor dashboard, registration, and commission tracking.</p>
                        <div class="project-tech">
                            <span class="tech-tag">Django REST</span>
                            <span class="tech-tag">Next.js</span>
                            <span class="tech-tag">Ant Design</span>
                            <span class="tech-tag">Tailwind CSS</span>
                        </div>
                        <a href="https://arogya.bkarogyam.com/" class="project-link">View Project</a>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-content">
                        <h3 class="project-title">PR Web Techno</h3>
                        <p class="project-description">Digital marketing websites providing services, pricing details, and online payments with PayPal integration.</p>
                        <div class="project-tech">
                            <span class="tech-tag">Django</span>
                            <span class="tech-tag">Next.js</span>
                            <span class="tech-tag">PayPal API</span>
                            <span class="tech-tag">Tailwind CSS</span>
                        </div>
                        <a href="https://www.prwebtechno.com/" class="project-link">View Project</a>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-content">
                        <h3 class="project-title">MindForge</h3>
                        <p class="project-description">Tech blog platform with user reviews, ratings, and social sharing capabilities.</p>
                        <div class="project-tech">
                            <span class="tech-tag">Django</span>
                            <span class="tech-tag">Next.js</span>
                            <span class="tech-tag">Ant Design</span>
                            <span class="tech-tag">WebSockets</span>
                        </div>
                        <a href="https://pritans.pythonanywhere.com/" class="project-link">View Project</a>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-content">
                        <h3 class="project-title">Elections Management</h3>
                        <p class="project-description">Comprehensive election management platform with information hub and campaign booking system.</p>
                        <div class="project-tech">
                            <span class="tech-tag">Django</span>
                            <span class="tech-tag">Bootstrap</span>
                            <span class="tech-tag">JavaScript</span>
                            <span class="tech-tag">AWS</span>
                        </div>
                        <a href="https://www.electionsmanagement.com/" class="project-link">View Project</a>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-content">
                        <h3 class="project-title">Healthcare ERP</h3>
                        <p class="project-description">Comprehensive Healthcare ERP platform to streamline hospital operations including patient management, billing, and analytics.</p>
                        <div class="project-tech">
                            <span class="tech-tag">Django</span>
                            <span class="tech-tag">Next.js</span>
                            <span class="tech-tag">PostgreSQL</span>
                            <span class="tech-tag">Docker</span>
                        </div>
                        <a href="https://erp.bkarogyam.com/" class="project-link">View Project</a>
                    </div>
                </div>
                
            </div>
        </div>
    </section>

    <section id="education">
        <div class="container">
            <h2 class="section-title">Education</h2>
            <div class="experience-item">
                <div class="experience-header">
                    <span class="company">Allahabad College of Engineering & Management</span>
                    <span class="date">2017</span>
                </div>
                <div class="position">Diploma in Computer Science</div>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <p>© 2023 Pritesh Prasad. All rights reserved.</p>
            <p>Contact: priteshrao3@gmail.com | +91-9170475552</p>
        </div>
    </footer>
</body>
</html>
