<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jean Paul Castañeda · Frontend Developer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #0D0D0D;
            --secondary: #1a1a1a;
            --accent: #5b21b6;
            --text: #ffffff;
            --text-light: #d1d5db;
            --border: #3f3f46;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', 'Oxygen', 'Ubuntu', 'Cantarell', 'Fira Sans', 'Droid Sans', 'Helvetica Neue', sans-serif;
            background: var(--primary);
            color: var(--text);
            line-height: 1.6;
            padding: 2rem;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
        }

        h1 {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
            letter-spacing: -0.02em;
        }

        h2 {
            font-size: 1.75rem;
            font-weight: 600;
            margin-top: 2rem;
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
            gap: 0.75rem;
            color: var(--text);
        }

        h3 {
            font-size: 1.25rem;
            font-weight: 600;
            margin-top: 1.5rem;
            margin-bottom: 0.75rem;
            color: var(--text);
        }

        h4 {
            font-size: 1rem;
            font-weight: 600;
            margin-top: 1rem;
            margin-bottom: 0.75rem;
            color: var(--text-light);
        }

        .tagline {
            font-size: 1.125rem;
            font-style: italic;
            color: var(--text-light);
            margin-bottom: 1.5rem;
            padding: 1rem;
            border-left: 3px solid var(--accent);
            background: var(--secondary);
        }

        .meta {
            font-size: 0.95rem;
            color: var(--text-light);
            margin-bottom: 2rem;
            line-height: 1.8;
        }

        a {
            color: var(--accent);
            text-decoration: none;
            font-weight: 500;
        }

        a:hover {
            text-decoration: underline;
        }

        .section-divider {
            width: 100%;
            height: 1px;
            background: var(--border);
            margin: 2rem 0;
        }

        .about-text {
            font-size: 1rem;
            line-height: 1.8;
            margin-bottom: 1.5rem;
            color: var(--text-light);
        }

        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1rem;
            margin-bottom: 1.5rem;
        }

        .stat-box {
            background: var(--secondary);
            padding: 1rem;
            border-radius: 6px;
            border-left: 3px solid var(--accent);
        }

        .stat-label {
            font-size: 0.85rem;
            color: var(--text-light);
            text-transform: uppercase;
            letter-spacing: 0.05em;
            margin-bottom: 0.5rem;
        }

        .stat-value {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--text);
        }

        .stack-category {
            margin-bottom: 1.5rem;
        }

        .stack-category h4 {
            color: var(--accent);
            margin-bottom: 0.75rem;
        }

        .stack-items {
            display: flex;
            flex-wrap: wrap;
            gap: 0.75rem;
            margin-bottom: 0.5rem;
        }

        .tech-tag {
            display: inline-block;
            background: var(--secondary);
            padding: 0.5rem 1rem;
            border-radius: 4px;
            font-size: 0.9rem;
            border: 1px solid var(--border);
        }

        .experience-item {
            margin-bottom: 2.5rem;
        }

        .exp-header {
            display: flex;
            justify-content: space-between;
            align-items: baseline;
            margin-bottom: 0.75rem;
        }

        .exp-company {
            font-size: 1.1rem;
            font-weight: 600;
            color: var(--text);
        }

        .exp-date {
            font-size: 0.9rem;
            color: var(--text-light);
        }

        .exp-role {
            font-size: 1rem;
            font-weight: 600;
            color: var(--accent);
            margin-bottom: 0.5rem;
        }

        .exp-description {
            font-size: 0.95rem;
            color: var(--text-light);
            margin-bottom: 1rem;
        }

        .project-list {
            margin: 1rem 0;
        }

        .project-item {
            padding: 0.75rem 0;
            border-bottom: 1px solid var(--border);
            font-size: 0.95rem;
        }

        .project-item:last-child {
            border-bottom: none;
        }

        .project-name {
            font-weight: 600;
            color: var(--text);
        }

        .project-desc {
            color: var(--text-light);
            margin-left: 1rem;
            display: inline;
        }

        .responsibilities {
            list-style: none;
            margin: 1rem 0;
        }

        .responsibilities li {
            padding: 0.5rem 0 0.5rem 1.5rem;
            position: relative;
            font-size: 0.95rem;
            color: var(--text-light);
            line-height: 1.6;
        }

        .responsibilities li:before {
            content: "→";
            position: absolute;
            left: 0;
            color: var(--accent);
            font-weight: bold;
        }

        .certifications {
            list-style: none;
            margin: 1rem 0;
        }

        .certifications li {
            padding: 0.75rem 0;
            border-bottom: 1px solid var(--border);
            font-size: 0.95rem;
        }

        .certifications li:last-child {
            border-bottom: none;
        }

        .cert-name {
            font-weight: 600;
            color: var(--text);
        }

        .cert-year {
            color: var(--text-light);
            font-size: 0.85rem;
            margin-left: 0.5rem;
        }

        .cert-desc {
            color: var(--text-light);
            font-size: 0.9rem;
            margin-top: 0.25rem;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            margin: 1.5rem 0;
            font-size: 0.95rem;
        }

        th, td {
            padding: 1rem;
            text-align: left;
            border-bottom: 1px solid var(--border);
        }

        th {
            background: var(--secondary);
            font-weight: 600;
            color: var(--text);
        }

        td {
            color: var(--text-light);
        }

        .language-item {
            margin-bottom: 1.5rem;
            padding-left: 1.5rem;
            position: relative;
        }

        .language-item:before {
            content: "/";
            position: absolute;
            left: 0;
            color: var(--accent);
            font-weight: bold;
            font-size: 1.25rem;
        }

        .lang-name {
            font-weight: 600;
            color: var(--text);
        }

        .lang-level {
            color: var(--text-light);
            font-size: 0.9rem;
        }

        .contact-list {
            list-style: none;
            margin: 1.5rem 0;
        }

        .contact-list li {
            padding: 0.75rem 0;
            font-size: 0.95rem;
            display: flex;
            align-items: center;
            gap: 0.75rem;
        }

        .emoji {
            font-size: 1.1rem;
            min-width: 1.5rem;
        }

        .footer {
            text-align: center;
            margin-top: 3rem;
            padding-top: 2rem;
            border-top: 1px solid var(--border);
            color: var(--text-light);
            font-size: 0.9rem;
        }

        .footer-text {
            margin-bottom: 0.5rem;
            font-style: italic;
        }

        .footer-credit {
            font-weight: 600;
            color: var(--text);
        }

        @media (max-width: 768px) {
            body {
                padding: 1.5rem;
            }

            h1 {
                font-size: 2rem;
            }

            h2 {
                font-size: 1.5rem;
            }

            .exp-header {
                flex-direction: column;
                align-items: flex-start;
            }

            .exp-date {
                margin-top: 0.5rem;
            }

            .stats {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <h1>Jean Paul Castañeda</h1>
        <h2 style="margin-top: 0; font-size: 1.25rem; color: var(--text-light);">Frontend Developer</h2>

        <div class="tagline">Construyo interfaces rápidas, modernas y pensadas para durar.</div>

        <div class="meta">
            Frontend developer y founder de <strong><a href="https://www.404studios.es">404studios</a></strong><br>
            Especializado en <strong>React</strong>, <strong>Next.js</strong> y <strong>TypeScript</strong><br>
            QA Automation en <strong>Softek</strong>
        </div>

        <!-- About Section -->
        <h2>🎯 About</h2>
        <div class="about-text">
            No me interesa solo "hacer webs bonitas". Me interesa construir productos que se sientan <strong>rápidos, claros y sólidos</strong> cuando alguien los usa de verdad.
        </div>

        <div class="stats">
            <div class="stat-box">
                <div class="stat-label">Años en producción</div>
                <div class="stat-value">+2</div>
            </div>
            <div class="stat-box">
                <div class="stat-label">Clientes activos</div>
                <div class="stat-value">+5</div>
            </div>
            <div class="stat-box">
                <div class="stat-label">Lighthouse avg</div>
                <div class="stat-value">90+</div>
            </div>
            <div class="stat-box">
                <div class="stat-label">Ubicación</div>
                <div class="stat-value">Madrid, ES</div>
            </div>
        </div>

        <div class="about-text">
            Trabajo en el ecosistema <strong>React moderno</strong>: interfaces escalables, animaciones fluidas, arquitectura limpia y optimización real. Mi experiencia en <strong>QA automation</strong> influye directamente en cómo desarrollo—pienso siempre en estabilidad, testing y mantenimiento a largo plazo.
        </div>

        <div class="section-divider"></div>

        <!-- Stack Section -->
        <h2>🛠️ Stack & Expertise</h2>

        <div class="stack-category">
            <h4>Frontend · UI · Motion</h4>
            <div class="stack-items">
                <span class="tech-tag">React 18</span>
                <span class="tech-tag">Next.js 15</span>
                <span class="tech-tag">TypeScript</span>
                <span class="tech-tag">Tailwind CSS</span>
                <span class="tech-tag">SCSS/SASS</span>
                <span class="tech-tag">Framer Motion</span>
                <span class="tech-tag">GSAP</span>
                <span class="tech-tag">Vite</span>
            </div>
        </div>

        <div class="stack-category">
            <h4>Backend · Data</h4>
            <div class="stack-items">
                <span class="tech-tag">Firebase</span>
                <span class="tech-tag">Supabase</span>
                <span class="tech-tag">REST APIs</span>
                <span class="tech-tag">TanStack Query</span>
            </div>
        </div>

        <div class="stack-category">
            <h4>QA · Testing</h4>
            <div class="stack-items">
                <span class="tech-tag">Cypress</span>
                <span class="tech-tag">Jest</span>
                <span class="tech-tag">Page Object Model</span>
                <span class="tech-tag">E2E Automation</span>
            </div>
        </div>

        <div class="stack-category">
            <h4>Performance & SEO</h4>
            <div class="stack-items">
                <span class="tech-tag">Lighthouse</span>
                <span class="tech-tag">Core Web Vitals</span>
                <span class="tech-tag">Technical SEO</span>
                <span class="tech-tag">Accessibility</span>
            </div>
        </div>

        <div class="stack-category">
            <h4>AI Workflow</h4>
            <div class="stack-items">
                <span class="tech-tag">Cursor</span>
                <span class="tech-tag">Claude Code</span>
                <span class="tech-tag">GitHub Copilot</span>
            </div>
        </div>

        <div class="section-divider"></div>

        <!-- Experience Section -->
        <h2>💼 Experience</h2>

        <div class="experience-item">
            <div class="exp-header">
                <div>
                    <div class="exp-company"><a href="https://www.404studios.es">404studios</a></div>
                    <div class="exp-role">Frontend Developer & Founder</div>
                </div>
                <div class="exp-date">Jan 2024 → Present</div>
            </div>

            <div class="exp-description">
                Diseño y desarrollo de aplicaciones web para e-commerce, plataformas de servicios y productos digitales.
            </div>

            <h4>Live projects</h4>
            <div class="project-list">
                <div class="project-item">
                    <span class="project-name"><a href="https://www.wktravel.es">Winking Travel</a></span>
                    <span class="project-desc">Agencia de viajes a medida · Next.js + Firebase</span>
                </div>
                <div class="project-item">
                    <span class="project-name"><a href="https://yimailife.es">YIMAILIFE</a></span>
                    <span class="project-desc">E-commerce B2B multilenguaje · Packaging & HORECA</span>
                </div>
                <div class="project-item">
                    <span class="project-name"><a href="https://www.donalexa.com">Donalexa</a></span>
                    <span class="project-desc">E-commerce · Donas premium</span>
                </div>
                <div class="project-item">
                    <span class="project-name"><a href="https://hdsound.es">HD Sound</a></span>
                    <span class="project-desc">Landing + lead capture · DJ bodas</span>
                </div>
                <div class="project-item">
                    <span class="project-name"><a href="https://ohannausa.com">Ohanna USA</a></span>
                    <span class="project-desc">E-commerce interactivo</span>
                </div>
                <div class="project-item">
                    <span class="project-name"><a href="https://wjastudios.com">WJA Studios</a></span>
                    <span class="project-desc">Web corporativa</span>
                </div>
            </div>

            <h4>Responsibilities</h4>
            <ul class="responsibilities">
                <li>Mobile-first UI/UX · Responsive design & user experience</li>
                <li>Performance optimization · Core Web Vitals & Lighthouse scores</li>
                <li>Firebase & REST APIs · Dynamic features & data management</li>
                <li>Motion design · Animations (Framer Motion, GSAP)</li>
                <li>Technical SEO & accessibility audits</li>
            </ul>
        </div>

        <div class="experience-item">
            <div class="exp-header">
                <div>
                    <div class="exp-company">Softek</div>
                    <div class="exp-role">QA Engineer</div>
                </div>
                <div class="exp-date">Feb 2025 → Sep 2026</div>
            </div>

            <div class="exp-description">
                E2E testing, test automation, and quality assurance.
            </div>

            <ul class="responsibilities">
                <li>Cypress automation · Page Object Model · TypeScript test suites</li>
                <li>E2E validation · Authentication & critical user flows</li>
                <li>Cross-team collaboration · Documentation & issue tracking (Jira)</li>
            </ul>
        </div>

        <div class="section-divider"></div>

        <!-- Training & Certifications -->
        <h2>🎓 Training & Certifications</h2>

        <ul class="certifications">
            <li>
                <span class="cert-name">Google AI Professional Certificate</span>
                <span class="cert-year">2026</span>
                <div class="cert-desc">IA, automation, AI-assisted workflows</div>
            </li>
            <li>
                <span class="cert-name">IBM SkillsBuild: Retrieval-Augmented Generation</span>
                <span class="cert-year">2026</span>
                <div class="cert-desc">LLM systems & RAG architecture</div>
            </li>
            <li>
                <span class="cert-name">IBM SkillsBuild: Cybersecurity Fundamentals</span>
                <span class="cert-year">2026</span>
            </li>
            <li>
                <span class="cert-name">Desarrollo de Aplicaciones Web · IFCD0210</span>
                <span class="cert-year">2024</span>
                <div class="cert-desc">590 hours · Official certification</div>
            </li>
            <li>
                <span class="cert-name">Licenciatura en Derecho</span>
                <div class="cert-desc">Universidad Bicentenaria de Araguaprevio</div>
            </li>
        </ul>

        <div class="section-divider"></div>

        <!-- Metrics -->
        <h2>📊 Metrics & Highlights</h2>

        <table>
            <thead>
                <tr>
                    <th>Metric</th>
                    <th>Value</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>Years in production</td>
                    <td>+2</td>
                </tr>
                <tr>
                    <td>Active projects</td>
                    <td>+5</td>
                </tr>
                <tr>
                    <td>Avg. Lighthouse score</td>
                    <td>90+</td>
                </tr>
                <tr>
                    <td>Tech stack breadth</td>
                    <td>Frontend, Backend, QA, AI Integration</td>
                </tr>
                <tr>
                    <td>Client satisfaction</td>
                    <td>Portfolio-driven</td>
                </tr>
            </tbody>
        </table>

        <div class="section-divider"></div>

        <!-- Languages -->
        <h2>🌐 Languages</h2>

        <div class="language-item">
            <div class="lang-name">Español</div>
            <div class="lang-level">Nativo</div>
        </div>

        <div class="language-item">
            <div class="lang-name">English</div>
            <div class="lang-level">B1 Intermediate — Fluent technical reading & writing</div>
        </div>

        <div class="section-divider"></div>

        <!-- Contact -->
        <h2>📬 Get in Touch</h2>

        <div class="about-text">
            Open to projects, collaborations, and opportunities where I can deliver <strong>solid frontend</strong>, <strong>good design judgment</strong>, and <strong>real attention to detail</strong>.
        </div>

        <ul class="contact-list">
            <li>
                <span class="emoji">📧</span>
                <span><strong>Email:</strong> <a href="mailto:hola@404studios.es">hola@404studios.es</a></span>
            </li>
            <li>
                <span class="emoji">🔗</span>
                <span><strong>Portfolio:</strong> <a href="https://www.404studios.es">404studios.es</a></span>
            </li>
            <li>
                <span class="emoji">💼</span>
                <span><strong>LinkedIn:</strong> <a href="https://www.linkedin.com/in/jeancastanedah/">jeancastanedah</a></span>
            </li>
            <li>
                <span class="emoji">🐙</span>
                <span><strong>GitHub:</strong> <a href="https://github.com/Arrobajean">@Arrobajean</a></span>
            </li>
        </ul>

        <!-- Footer -->
        <div class="footer">
            <div class="footer-text">Always building for performance, quality, and real user needs.</div>
            <div class="footer-credit">404studios · Madrid, Spain · 2026</div>
        </div>
    </div>
</body>
</html>
