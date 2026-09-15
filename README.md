# Flow Zenix

Official website of Flow Zenix — AI Automation & Business Systems Consultancy.

🌐 Live site: https://flowzenix.xyz
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flow Zenix | AI-Powered Business Automation Partner</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-navy: #071A33;
            --secondary-gold: #E5A900;
            --bg-ivory: #F8F5ED;
            --white: #FFFFFF;
            --text-dark: #0D1B2A;
            --text-muted: #4A5568;
            --border-light: #E2E8F0;
            --accent-green: #2D6A4F;
            --container-width: 1100px;
            --transition-speed: 0.3s;
            --radius-card: 16px;
            --radius-btn: 8px;
            --header-bg: rgba(248, 245, 237, 0.95);
        }

        /* DARK MODE VARIABLES */
        body.dark-mode {
            --primary-navy: #102A43;
            --secondary-gold: #F2C94C;
            --bg-ivory: #0B131F;
            --white: #16222F;
            --text-dark: #F0F4F8;
            --text-muted: #9FB3C8;
            --border-light: #243B53;
            --accent-green: #3E885B;
            --header-bg: rgba(11, 19, 31, 0.95);
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--bg-ivory);
            color: var(--text-dark);
            line-height: 1.6;
            transition: background-color var(--transition-speed), color var(--transition-speed);
        }

        .container {
            max-width: var(--container-width);
            margin: 0 auto;
            padding: 0 20px;
        }

        h1, h2, h3, h4 {
            color: var(--text-dark);
            font-weight: 700;
            line-height: 1.25;
        }

        h1 { font-size: 2.5rem; }
        h2 { font-size: 1.85rem; margin-bottom: 1rem; }
        h3 { font-size: 1.25rem; margin-bottom: 0.5rem; }

        p {
            font-size: 0.95rem;
            color: var(--text-muted);
            margin-bottom: 1rem;
        }

        .eyebrow {
            display: block;
            font-size: 0.75rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 0.1em;
            color: var(--secondary-gold);
            margin-bottom: 0.5rem;
        }

        .text-center { text-align: center; }

        /* Buttons */
        .btn {
            display: inline-block;
            padding: 12px 24px;
            font-size: 0.9rem;
            font-weight: 600;
            text-decoration: none;
            border-radius: var(--radius-btn);
            transition: all var(--transition-speed);
            cursor: pointer;
            border: 1px solid transparent;
        }

        .btn-primary {
            background-color: var(--secondary-gold);
            color: #071A33;
        }

        .btn-primary:hover {
            background-color: var(--text-dark);
            color: var(--bg-ivory);
        }

        .btn-secondary {
            background-color: transparent;
            border: 1px solid var(--text-dark);
            color: var(--text-dark);
        }

        .btn-secondary:hover {
            background-color: var(--text-dark);
            color: var(--bg-ivory);
        }

        /* Dark Mode Toggle Button */
        .theme-toggle-btn {
            background: transparent;
            border: 1px solid var(--border-light);
            color: var(--text-dark);
            padding: 8px 12px;
            border-radius: var(--radius-btn);
            cursor: pointer;
            font-size: 0.85rem;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 6px;
            transition: all var(--transition-speed);
        }

        .theme-toggle-btn:hover {
            border-color: var(--secondary-gold);
            color: var(--secondary-gold);
        }

        /* Global Header Nav */
        header {
            background-color: var(--header-bg);
            border-bottom: 1px solid var(--border-light);
            padding: 16px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            backdrop-filter: blur(8px);
            transition: background-color var(--transition-speed);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo-container {
            display: flex;
            align-items: center;
        }

        .logo-img {
            height: 40px; /* প্রয়োজনমতো লোগোর হাইট অ্যাডজাস্ট করুন */
            width: auto;
            display: block;
        }

        .nav-links {
            display: flex;
            gap: 24px;
            align-items: center;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 600;
            font-size: 0.9rem;
            transition: color var(--transition-speed);
        }

        .nav-links a:hover {
            color: var(--secondary-gold);
        }

        .nav-actions {
            display: flex;
            gap: 12px;
            align-items: center;
        }

        /* Sections General */
        .page-section {
            padding: 60px 0;
            border-bottom: 1px solid var(--border-light);
        }

        .grid-2 { display: grid; grid-template-columns: 1fr 1fr; gap: 32px; align-items: center; }
        .grid-3 { display: grid; grid-template-columns: repeat(3, 1fr); gap: 20px; margin-top: 24px; }
        .grid-4 { display: grid; grid-template-columns: repeat(4, 1fr); gap: 16px; margin-top: 24px; }

        .card {
            background: var(--white);
            padding: 24px;
            border-radius: var(--radius-card);
            border: 1px solid var(--border-light);
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.03);
            transition: transform var(--transition-speed), box-shadow var(--transition-speed), background-color var(--transition-speed);
        }

        .card:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.08);
        }

        /* Interactive Workflow Canvas */
        .workflow-canvas {
            background: var(--primary-navy);
            border-radius: var(--radius-card);
            padding: 20px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
            color: #FFFFFF;
        }

        .workflow-title {
            font-size: 0.75rem;
            color: var(--secondary-gold);
            text-transform: uppercase;
            letter-spacing: 0.05em;
            margin-bottom: 12px;
            font-weight: 700;
        }

        .interactive-nodes {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .wf-node {
            background: rgba(255, 255, 255, 0.06);
            border: 1px solid rgba(255, 255, 255, 0.15);
            padding: 12px 16px;
            border-radius: 8px;
            cursor: pointer;
            transition: all var(--transition-speed);
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 0.85rem;
            color: #FFFFFF;
        }

        .wf-node:hover, .wf-node.active {
            background: rgba(229, 169, 0, 0.15);
            border-color: var(--secondary-gold);
        }

        .node-tag {
            font-size: 0.65rem;
            background: var(--secondary-gold);
            color: #071A33;
            padding: 2px 6px;
            border-radius: 4px;
            font-weight: 700;
        }

        .node-details {
            margin-top: 14px;
            background: rgba(255, 255, 255, 0.04);
            padding: 12px;
            border-radius: 8px;
            border-left: 3px solid var(--secondary-gold);
            font-size: 0.8rem;
            line-height: 1.4;
            min-height: 60px;
            color: rgba(255, 255, 255, 0.9);
        }

        /* Comparison Section */
        .comparison-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin-top: 24px;
        }

        .comparison-card {
            padding: 24px;
            border-radius: var(--radius-card);
            border: 1px solid var(--border-light);
        }

        .comparison-card.before {
            background: rgba(239, 68, 68, 0.05);
            border-color: rgba(239, 68, 68, 0.2);
        }

        .comparison-card.after {
            background: rgba(45, 106, 79, 0.08);
            border-color: rgba(45, 106, 79, 0.3);
        }

        .comparison-card h4 { margin-bottom: 12px; }
        .comparison-card.before h4 { color: #DC2626; }
        .comparison-card.after h4 { color: var(--accent-green); }

        .comparison-list { list-style: none; font-size: 0.85rem; }
        .comparison-list li { margin-bottom: 8px; padding-left: 18px; position: relative; }
        .comparison-card.before li::before { content: "✕"; position: absolute; left: 0; color: #DC2626; }
        .comparison-card.after li::before { content: "✓"; position: absolute; left: 0; color: var(--accent-green); }

        /* Quiz Section */
        .quiz-container {
            max-width: 600px;
            margin: 24px auto 0;
            background: var(--white);
            border-radius: var(--radius-card);
            border: 1px solid var(--border-light);
            padding: 28px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.03);
        }

        .progress-bar-wrap {
            width: 100%;
            height: 5px;
            background: var(--border-light);
            border-radius: 10px;
            margin-bottom: 20px;
            overflow: hidden;
        }

        .progress-bar {
            height: 100%;
            width: 33%;
            background: var(--secondary-gold);
            transition: width 0.4s ease;
        }

        .quiz-step { display: none; }
        .quiz-step.active { display: block; }

        .quiz-options {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 10px;
            margin: 16px 0;
        }

        .quiz-option-btn {
            background: var(--bg-ivory);
            border: 1px solid var(--border-light);
            padding: 12px;
            border-radius: 8px;
            text-align: left;
            font-weight: 600;
            font-size: 0.85rem;
            color: var(--text-dark);
            cursor: pointer;
            transition: all var(--transition-speed);
        }

        .quiz-option-btn:hover, .quiz-option-btn.selected {
            border-color: var(--secondary-gold);
            background: rgba(229, 169, 0, 0.15);
        }

        .quiz-options-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 12px;
            margin-top: 16px;
        }

        .quiz-card-btn {
            display: flex;
            align-items: center;
            gap: 14px;
            padding: 14px 16px;
            background: var(--bg-ivory);
            border: 1.5px solid var(--border-light);
            border-radius: 10px;
            text-align: left;
            cursor: pointer;
            transition: all 0.25s ease;
            width: 100%;
        }

        .quiz-card-btn:hover, .quiz-card-btn.selected {
            border-color: var(--secondary-gold);
            background: rgba(229, 169, 0, 0.08);
            transform: translateY(-2px);
        }

        .quiz-card-icon { font-size: 1.5rem; }
        .quiz-card-title { display: block; font-weight: 700; font-size: 0.9rem; color: var(--text-dark); }
        .quiz-card-sub { display: block; font-size: 0.78rem; color: var(--text-muted); margin-top: 2px; }

        /* Form Inputs */
        .input-group {
            display: flex;
            flex-direction: column;
            gap: 6px;
            margin-bottom: 14px;
            text-align: left;
        }

        .input-group label {
            font-size: 0.8rem;
            font-weight: 600;
            color: var(--text-dark);
        }

        .input-group input, .input-group textarea, .input-group select {
            padding: 12px;
            border: 1px solid var(--border-light);
            border-radius: 8px;
            font-size: 0.85rem;
            font-family: inherit;
            background-color: var(--bg-ivory);
            color: var(--text-dark);
        }

        .input-group textarea {
            resize: vertical;
            min-height: 100px;
        }

        .enhanced-select {
            width: 100%;
            padding: 12px 14px;
            border: 1.5px solid var(--border-light);
            border-radius: 8px;
            background-color: var(--bg-ivory);
            color: var(--text-dark);
            font-size: 0.85rem;
            font-weight: 500;
            outline: none;
            transition: border-color 0.3s ease;
        }

        .enhanced-select:focus {
            border-color: var(--secondary-gold);
        }

        .service-hint {
            margin-top: 8px;
            padding: 10px 12px;
            background: rgba(229, 169, 0, 0.1);
            border-left: 3px solid var(--secondary-gold);
            border-radius: 6px;
            font-size: 0.8rem;
            color: var(--text-dark);
            display: block;
        }

        /* Contact Section */
        .contact-container {
            max-width: 650px;
            margin: 24px auto 0;
            background: var(--white);
            padding: 32px;
            border-radius: var(--radius-card);
            border: 1px solid var(--border-light);
        }

        .direct-email-link {
            color: var(--secondary-gold);
            font-weight: 600;
            text-decoration: underline;
        }

        /* Footer */
        footer {
            background-color: #040D1A;
            color: #FFFFFF;
            padding: 50px 0 20px;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: 2fr 1fr 1fr;
            gap: 40px;
            margin-bottom: 30px;
        }

        .footer-brand .logo-container { margin-bottom: 10px; }
        .footer-brand p { color: rgba(255, 255, 255, 0.7); font-size: 0.85rem; margin-top: 8px; }

        .footer-column h4 {
            color: var(--secondary-gold);
            font-size: 0.9rem;
            margin-bottom: 12px;
            text-transform: uppercase;
            letter-spacing: 0.05em;
        }

        .footer-links { list-style: none; }
        .footer-links li { margin-bottom: 8px; }
        .footer-links a {
            color: rgba(255, 255, 255, 0.8);
            text-decoration: none;
            font-size: 0.85rem;
            transition: color var(--transition-speed);
        }

        .footer-links a:hover { color: var(--secondary-gold); }

        .footer-bottom {
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            padding-top: 20px;
            text-align: center;
            font-size: 0.8rem;
            color: rgba(255, 255, 255, 0.5);
        }

        @media (max-width: 768px) {
            .grid-2, .grid-3, .grid-4, .comparison-grid, .quiz-options, .footer-grid { grid-template-columns: 1fr; }
            .nav-links { display: none; }
            h1 { font-size: 2rem; }
        }
    </style>
</head>
<body>

    <!-- GLOBAL NAVIGATION -->
    <header>
        <div class="container">
            <nav>
                <!-- Image Logo Section -->
                <div class="logo-container">
                    <a href="http://flowzenix.xyz/">
                        <img src="logo.png" alt="Flow Zenix Logo" class="logo-img">
                    </a>
                </div>
                <div class="nav-links">
                    <a href="#home">Home</a>
                    <a href="#services">Services</a>
                    <a href="#solutions">Solutions</a>
                    <a href="#about">About</a>
                    <a href="#contact">Contact</a>
                </div>
                <div class="nav-actions">
                    <button class="theme-toggle-btn" id="themeToggle" onclick="toggleDarkMode()">
                        <span id="themeIcon">🌙</span> <span id="themeText">Dark</span>
                    </button>
                    <a href="#contact" class="btn btn-primary">Book Consultation</a>
                </div>
            </nav>
        </div>
    </header>

    <!-- PAGE 1: HOME -->
    <section id="home" class="page-section">
        <div class="container">
            <div class="grid-2">
                <div>
                    <span class="eyebrow">AI-POWERED BUSINESS AUTOMATION</span>
                    <h1>Turn Repetitive Work Into Intelligent Systems.</h1>
                    <p style="margin-top: 12px;">Flow Zenix helps businesses automate repetitive operations, connect their tools, and use AI to build faster, smarter, and more scalable workflows.</p>
                    <div style="display: flex; gap: 12px; margin-top: 16px;">
                        <a href="#contact" class="btn btn-primary">Book a Free Consultation</a>
                        <a href="#services" class="btn btn-secondary">Explore Our Services</a>
                    </div>
                </div>

                <div class="workflow-canvas">
                    <div class="workflow-title">⚡ Abstract Connected Workflow Diagram</div>
                    <div class="interactive-nodes">
                        <div class="wf-node active" onclick="showNodeDetails(event, 'trigger')">
                            <span>1. App Data & Form Ingest</span>
                            <span class="node-tag">INPUT</span>
                        </div>
                        <div class="wf-node" onclick="showNodeDetails(event, 'agent')">
                            <span>2. AI Processing Node</span>
                            <span class="node-tag">AI ENGINE</span>
                        </div>
                        <div class="wf-node" onclick="showNodeDetails(event, 'action')">
                            <span>3. Automated Action / CRM</span>
                            <span class="node-tag">OUTPUT</span>
                        </div>
                    </div>
                    <div class="node-details" id="node-info-text">
                        <strong>Event Trigger:</strong> Captures data from webhooks, web forms, emails, or APIs instantly without manual entry.
                    </div>
                </div>
            </div>

            <!-- Problem Section -->
            <div style="margin-top: 60px;" class="text-center">
                <span class="eyebrow">OPERATIONAL BOTTLENECKS</span>
                <h2>Your Team Shouldn't Spend Its Best Hours on Repetitive Work.</h2>
                <div class="grid-4">
                    <div class="card">
                        <h3>Manual Data Entry</h3>
                        <p>Copy-pasting records between spreadsheets, CRMs, and email platforms.</p>
                    </div>
                    <div class="card">
                        <h3>Delayed Follow-ups</h3>
                        <p>Leads cooling down while waiting for manual review and routing.</p>
                    </div>
                    <div class="card">
                        <h3>Fragmented Apps</h3>
                        <p>Disconnected web software forcing team members to act as middleware.</p>
                    </div>
                    <div class="card">
                        <h3>Static Reporting</h3>
                        <p>Hours wasted compiling weekly status reports manually across tools.</p>
                    </div>
                </div>
            </div>

            <!-- Process Framework -->
            <div style="margin-top: 60px;" class="text-center">
                <span class="eyebrow">OUR METHODOLOGY</span>
                <h2>Process First. Automation Second.</h2>
                <div class="grid-3">
                    <div class="card">
                        <h3>01 Discover</h3>
                        <p>Audit existing operations to surface high-impact automation targets.</p>
                    </div>
                    <div class="card">
                        <h3>02 Automate</h3>
                        <p>Engineer resilient, low-latency workflow pipelines using custom scripts & AI.</p>
                    </div>
                    <div class="card">
                        <h3>03 Optimize</h3>
                        <p>Continuously monitor system performance, error rates, and throughput.</p>
                    </div>
                </div>
            </div>

            <!-- Visual Comparison Section -->
            <div style="margin-top: 60px;">
                <div class="text-center">
                    <span class="eyebrow">TRANSFORMATION</span>
                    <h2>Before vs. After Flow Zenix</h2>
                </div>
                <div class="comparison-grid">
                    <div class="comparison-card before">
                        <h4>BEFORE (Manual Friction)</h4>
                        <ul class="comparison-list">
                            <li>7-step manual friction process</li>
                            <li>Manual email drafting and lead qualification</li>
                            <li>Data copy-pasted across spreadsheets</li>
                            <li>Delayed customer response time (24+ hours)</li>
                        </ul>
                    </div>
                    <div class="comparison-card after">
                        <h4>AFTER (AI-Driven Stream)</h4>
                        <ul class="comparison-list">
                            <li>Instant AI parsing & lead qualification</li>
                            <li>Automated CRM synchronization</li>
                            <li>Personalized AI follow-up generated in seconds</li>
                            <li>Sub-10 second execution stream</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- PAGE 2: SERVICES -->
    <section id="services" class="page-section">
        <div class="container">
            <div class="text-center">
                <span class="eyebrow">OUR CAPABILITIES</span>
                <h2>Practical Automation & Modern Web Development</h2>
                <p>End-to-end operational systems, custom AI integrations, and responsive web platforms built to scale capacity.</p>
            </div>

            <div class="grid-3">
                <div class="card">
                    <h3>Modern Web Design & Dev</h3>
                    <p>Designing lightning-fast, highly responsive, and user-centric websites optimized for seamless conversion and performance.</p>
                </div>
                <div class="card">
                    <h3>Custom AI Integration</h3>
                    <p>Embedding AI models (OpenAI, Claude, Gemini), custom chatbots, and intelligent automation seamlessly into your web apps.</p>
                </div>
                <div class="card">
                    <h3>AI Automation</h3>
                    <p>Converting unstructured data, documents, and manual routines into intelligent, automated AI processes.</p>
                </div>
                <div class="card">
                    <h3>n8n Workflow Automation</h3>
                    <p>Flexible end-to-end integration across web apps, databases, and LLMs using self-hosted pipeline architecture.</p>
                </div>
                <div class="card">
                    <h3>Custom AI Agents</h3>
                    <p>Autonomous research, decision-making, and execution systems tailored strictly to your unique business logic.</p>
                </div>
                <div class="card">
                    <h3>API Integrations</h3>
                    <p>Connecting CRMs, Google Workspace, forms, databases, and custom software smoothly with low-latency APIs.</p>
                </div>
                <div class="card">
                    <h3>Business Process Automation</h3>
                    <p>Operational redesign for scalable organizational efficiency and significantly reduced administrative overhead.</p>
                </div>
                <div class="card">
                    <h3>Content & Social Media Automation</h3>
                    <p>Automated asset creation, multi-platform publishing, intelligent auto-scheduling, and performance analytics.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- PAGE 3: SOLUTIONS & AUDIT QUIZ -->
    <section id="solutions" class="page-section">
        <div class="container">
            <div class="text-center">
                <span class="eyebrow">USE CASES</span>
                <h2>Solve the Bottleneck. Automate the Process.</h2>
            </div>

            <div class="grid-3">
                <div class="card">
                    <h3>Lead Management</h3>
                    <p>Instant AI qualification, CRM sync, and automated response within 30 seconds.</p>
                </div>
                <div class="card">
                    <h3>Customer Support</h3>
                    <p>Automated ticket triage, instant AI resolution, and smart escalation routing.</p>
                </div>
                <div class="card">
                    <h3>Content Operations</h3>
                    <p>Turning one core idea into multi-channel campaigns automatically.</p>
                </div>
                <div class="card">
                    <h3>Data & Reporting</h3>
                    <p>Eliminating manual data aggregation with real-time automated dashboards.</p>
                </div>
                <div class="card">
                    <h3>Internal Operations</h3>
                    <p>Back-office task clearing, document parsing, and onboarding systems.</p>
                </div>
                <div class="card">
                    <h3>AI Research</h3>
                    <p>Transforming hours of web research into structured, instant business insights.</p>
                </div>
            </div>

            <!-- Interactive Audit Quiz -->
            <div style="margin-top: 60px;">
                <div class="text-center">
                    <span class="eyebrow">INTERACTIVE AUDIT</span>
                    <h2>Find Out What Your Business Can Automate</h2>
                </div>

                <div class="quiz-container">
                    <div class="progress-bar-wrap">
                        <div class="progress-bar" id="quiz-progress"></div>
                    </div>

                    <form id="quizForm" onsubmit="event.preventDefault(); finishQuiz();">
                        <div class="quiz-step active" id="step-1">
                            <h3>1. What is your primary business type?</h3>
                            <div class="quiz-options">
                                <button type="button" class="quiz-option-btn" onclick="selectQuizOption(this, 1)">B2B Agency / Service</button>
                                <button type="button" class="quiz-option-btn" onclick="selectQuizOption(this, 1)">E-commerce / Retail</button>
                                <button type="button" class="quiz-option-btn" onclick="selectQuizOption(this, 1)">SaaS / Tech Startup</button>
                                <button type="button" class="quiz-option-btn" onclick="selectQuizOption(this, 1)">Other SME Business</button>
                            </div>
                        </div>

                        <!-- ENHANCED QUIZ STEP 2 -->
                        <div class="quiz-step" id="step-2">
                            <h3>2. What is your primary focus or bottleneck?</h3>
                            <div class="quiz-options-grid">
                                <button type="button" class="quiz-card-btn" onclick="selectQuizOption(this, 2)">
                                    <div class="quiz-card-icon">🌐</div>
                                    <div class="quiz-card-content">
                                        <span class="quiz-card-title">New Website + AI Integration</span>
                                        <span class="quiz-card-sub">Modern Web Design, Custom AI Chatbot, or Intelligent Forms.</span>
                                    </div>
                                </button>
                                <button type="button" class="quiz-card-btn" onclick="selectQuizOption(this, 2)">
                                    <div class="quiz-card-icon">⚡</div>
                                    <div class="quiz-card-content">
                                        <span class="quiz-card-title">n8n Workflow & API Sync</span>
                                        <span class="quiz-card-sub">Connecting CRM, Email, and Google Sheets automatically.</span>
                                    </div>
                                </button>
                                <button type="button" class="quiz-card-btn" onclick="selectQuizOption(this, 2)">
                                    <div class="quiz-card-icon">💬</div>
                                    <div class="quiz-card-content">
                                        <span class="quiz-card-title">AI Support Agent</span>
                                        <span class="quiz-card-sub">Train AI on your business knowledge base for 24/7 support.</span>
                                    </div>
                                </button>
                                <button type="button" class="quiz-card-btn" onclick="selectQuizOption(this, 2)">
                                    <div class="quiz-card-icon">🎯</div>
                                    <div class="quiz-card-content">
                                        <span class="quiz-card-title">Lead Qualification & CRM Sync</span>
                                        <span class="quiz-card-sub">Qualify website leads instantly using automated AI workflows.</span>
                                    </div>
                                </button>
                            </div>
                        </div>

                        <div class="quiz-step" id="step-3">
                            <h3>3. Where should we send your custom blueprint?</h3>
                            <div style="margin-top: 14px;">
                                <div class="input-group">
                                    <label>Your Name</label>
                                    <input type="text" required placeholder="John Doe">
                                </div>
                                <div class="input-group">
                                    <label>Business Email</label>
                                    <input type="email" required placeholder="john@company.com">
                                </div>
                            </div>
                            <button type="submit" class="btn btn-primary" style="width: 100%; margin-top: 8px;">Get Automation Blueprint</button>
                        </div>

                        <div style="display: flex; justify-content: space-between; margin-top: 16px;" id="quiz-nav">
                            <button type="button" class="btn btn-secondary" id="prevBtn" onclick="changeStep(-1)" style="visibility: hidden;">Back</button>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- PAGE 4: ABOUT -->
    <section id="about" class="page-section">
        <div class="container">
            <div class="grid-2">
                <div>
                    <span class="eyebrow">ABOUT FLOW ZENIX</span>
                    <h2>We Believe Better Businesses Start With Better Systems.</h2>
                    <p style="margin-top: 12px;"><strong>Manifesto:</strong> "Don't automate everything. Automate what matters."</p>
                    <p>Flow Zenix operates as an enterprise systems consultancy rather than an ad-hoc freelancer service. We build resilient operational infrastructure that allows founders, agencies, and ops teams to focus on strategic growth.</p>
                </div>

                <div class="card">
                    <span class="eyebrow">OUR TECH STACK TAXONOMY</span>
                    <ul style="list-style: none; margin-top: 10px; font-size: 0.9rem;">
                        <li style="margin-bottom: 8px;"><strong>Workflow Automation:</strong> n8n, Custom Node.js / Python Engines</li>
                        <li style="margin-bottom: 8px;"><strong>AI Models & Tools:</strong> OpenAI API, Claude, Gemini, Custom Vector Stores</li>
                        <li style="margin-bottom: 8px;"><strong>Web Stack:</strong> HTML5, CSS3, JavaScript, React, Webflow, Custom Web Apps</li>
                        <li style="margin-bottom: 8px;"><strong>Business Systems:</strong> PostgreSQL, Supabase, Airtable, HubSpot</li>
                        <li><strong>Communications:</strong> Webhooks, REST, GraphQL, Slack, Google Workspace API</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- PAGE 5: CONTACT -->
    <section id="contact" class="page-section">
        <div class="container text-center">
            <span class="eyebrow">GET IN TOUCH</span>
            <h2>What Would You Automate First?</h2>
            <p>Tell us about your biggest operational bottleneck, or write directly to <a href="mailto:info@flowzenix.xyz" class="direct-email-link">info@flowzenix.xyz</a></p>

            <div class="contact-container">
                <form id="contactForm" onsubmit="event.preventDefault(); submitContact();">
                    <div class="input-group">
                        <label>Name *</label>
                        <input type="text" id="contact-name" required placeholder="Full Name">
                    </div>
                    <div class="input-group">
                        <label>Company Email *</label>
                        <input type="email" id="contact-email" required placeholder="name@company.com">
                    </div>
                    <div class="input-group">
                        <label>Company Name</label>
                        <input type="text" id="contact-company" placeholder="Organization Name">
                    </div>
                    <div class="input-group">
                        <label>What would you like to automate or build? *</label>
                        <textarea id="contact-message" required placeholder="Describe your web design, AI integration, or workflow bottleneck needs..."></textarea>
                    </div>
                    <div class="input-group">
                        <label>Current Tools Used</label>
                        <input type="text" id="contact-tools" placeholder="e.g. WordPress, React, HubSpot, Google Sheets, Slack...">
                    </div>

                    <!-- ENHANCED SERVICE SELECT DROPDOWN -->
                    <div class="input-group">
                        <label for="contact-challenge">Primary Service Needed *</label>
                        <select id="contact-challenge" class="enhanced-select" onchange="updateServiceHint(this.value)">
                            <option value="web-design-ai" selected>🚀 Web Design & Custom AI Integration (Website + Chatbot/LLM)</option>
                            <option value="ai-agent">🤖 Custom AI Agents & LLM Workflow Development</option>
                            <option value="n8n-automation">⚡ Process Automation (n8n & API Integrations)</option>
                            <option value="data-pipeline">📊 Automated Reporting & Data Pipelines</option>
                        </select>
                        <div id="service-hint" class="service-hint">
                            💡 <strong>Web Design & AI:</strong> Clean UI/UX design, fast execution, and integrated LLM Chatbots or AI features.
                        </div>
                    </div>

                    <button type="submit" class="btn btn-primary" style="width: 100%; margin-top: 10px;">Send My Request</button>
                </form>

                <div style="margin-top: 24px; padding-top: 20px; border-top: 1px solid var(--border-light);">
                    <p style="font-size: 0.85rem; font-weight: 600;">Not Sure What to Automate?</p>
                    <p style="font-size: 0.8rem; margin-bottom: 10px;">Schedule an open business process audit call to highlight your top 3 high-ROI opportunities.</p>
                    <a href="#contact" class="btn btn-secondary" onclick="alert('Audit booking feature initialized!')">Book an Open Audit Call</a>
                </div>
            </div>
        </div>
    </section>

    <!-- GLOBAL FOOTER -->
    <footer>
        <div class="container">
            <div class="footer-grid">
                <div class="footer-brand">
                    <div class="logo-container">
                        <a href="http://flowzenix.xyz/">
                            <img src="logo.png" alt="Flow Zenix Logo" class="logo-img">
                        </a>
                    </div>
                    <p>Automate. Optimize. Advance.</p>
                    <p style="margin-top: 10px;">Empowering businesses with intelligent AI agents, modern web design, and enterprise-grade system automations.</p>
                    <p style="margin-top: 8px; font-size: 0.85rem;">
                        <a href="mailto:info@flowzenix.xyz" style="color: var(--secondary-gold); text-decoration: none;">info@flowzenix.xyz</a>
                    </p>
                </div>
                <div class="footer-column">
                    <h4>Navigation</h4>
                    <ul class="footer-links">
                        <li><a href="#home">Home</a></li>
                        <li><a href="#services">Services</a></li>
                        <li><a href="#solutions">Solutions</a></li>
                        <li><a href="#about">About</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h4>Connect</h4>
                    <ul class="footer-links">
                        <li><a href="https://www.linkedin.com/company/flowzenix/?viewAsMember=true" target="_blank" rel="noopener">LinkedIn</a></li>
                        <li><a href="https://www.facebook.com/flowzenix" target="_blank" rel="noopener">Facebook</a></li>
                    </ul>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2026 Flow Zenix. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <!-- INTERACTIVE SCRIPTS -->
    <script>
        // Dark Mode Logic
        function toggleDarkMode() {
            document.body.classList.toggle('dark-mode');
            const isDark = document.body.classList.contains('dark-mode');
            
            document.getElementById('themeIcon').innerText = isDark ? '☀️' : '🌙';
            document.getElementById('themeText').innerText = isDark ? 'Light' : 'Dark';
            
            localStorage.setItem('theme', isDark ? 'dark' : 'light');
        }

        // Keep Dark Mode state on refresh
        if (localStorage.getItem('theme') === 'dark') {
            document.body.classList.add('dark-mode');
            document.getElementById('themeIcon').innerText = '☀️';
            document.getElementById('themeText').innerText = 'Light';
        }

        // Node Details Toggle Script
        const nodeData = {
            'trigger': '<strong>1. App Data & Form Ingest:</strong> Captures data from webhooks, web forms, emails, or APIs instantly without manual entry.',
            'agent': '<strong>2. AI Processing Node:</strong> An intelligent agent analyzes unstructured data, qualifies leads, or runs decision logic using LLMs.',
            'action': '<strong>3. Automated Action / CRM:</strong> Updates CRM, dispatches notifications, writes custom email responses, and triggers follow-ups.'
        };

        function showNodeDetails(e, nodeKey) {
            document.querySelectorAll('.wf-node').forEach(node => node.classList.remove('active'));
            e.currentTarget.classList.add('active');
            document.getElementById('node-info-text').innerHTML = nodeData[nodeKey];
        }

        // Service Hint Update Function
        function updateServiceHint(selectedValue) {
            const hintBox = document.getElementById('service-hint');
            const hints = {
                'web-design-ai': '💡 <strong>Web Design & AI:</strong> Clean UI/UX design, fast execution, and integrated LLM Chatbots or AI features.',
                'ai-agent': '💡 <strong>AI Agents:</strong> Autonomous research, decision engines, and RAG/Vector database integration.',
                'n8n-automation': '💡 <strong>n8n Automation:</strong> Seamless API integration across CRMs, Google Sheets, and messaging apps.',
                'data-pipeline': '💡 <strong>Data Pipelines:</strong> Automated data collection, cleaning, and real-time dashboard sync.'
            };
            hintBox.innerHTML = hints[selectedValue] || '💡 Select a service to view estimated deliverables.';
        }

        // Quiz Logic Script
        let currentQuizStep = 1;

        function changeStep(direction) {
            document.getElementById(`step-${currentQuizStep}`).classList.remove('active');
            currentQuizStep += direction;
            document.getElementById(`step-${currentQuizStep}`).classList.add('active');

            const progressPercent = (currentQuizStep / 3) * 100;
            document.getElementById('quiz-progress').style.width = `${progressPercent}%`;

            document.getElementById('prevBtn').style.visibility = currentQuizStep > 1 ? 'visible' : 'hidden';
            if (currentQuizStep === 3) {
                document.getElementById('quiz-nav').style.display = 'none';
            } else {
                document.getElementById('quiz-nav').style.display = 'flex';
            }
        }

        function selectQuizOption(buttonElement, stepNumber) {
            const parent = buttonElement.parentElement;
            parent.querySelectorAll('.quiz-option-btn, .quiz-card-btn').forEach(btn => btn.classList.remove('selected'));
            buttonElement.classList.add('selected');

            setTimeout(() => {
                if (stepNumber < 3) changeStep(1);
            }, 300);
        }

        function finishQuiz() {
            alert('Thank you! Your custom automation roadmap has been dispatched to your email.');
        }

        function submitContact() {
            alert('Thank you for contacting Flow Zenix! We will evaluate your request and get back to you shortly.');
            document.getElementById('contactForm').reset();
        }
    </script>
</body>
</html>
