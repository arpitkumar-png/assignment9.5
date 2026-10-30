HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <!-- Viewport Meta Tag for Mobile Responsiveness -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tech Innovators — Portfolio-Ready Responsive Landing Page</title>
    <!-- Link to External Stylesheet -->
    <link rel="stylesheet" href="landing-style.css">
</head>
<body>

    <!-- --- Header & Responsive Navigation Bar --- -->
    <header class="site-header">
        <nav class="navbar">
            <div class="nav-logo">
                <a href="#">TechInnovators</a>
            </div>
            <ul class="nav-links">
                <li><a href="#hero">Home</a></li>
                <li><a href="#features">Features</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <div class="nav-cta">
                <a href="#contact" class="btn-primary">Join Community</a>
            </div>
        </nav>
    </header>

    <main class="main-content">
        
        <!-- --- Hero Section (Flexbox Alignment & Layout) --- -->
        <section id="hero" class="hero-section">
            <div class="hero-text-content">
                <span class="hero-badge">Portfolio Capstone 2026</span>
                <h1>Build Modern, Responsive Web Apps with Confidence</h1>
                <p>
                    Master HTML, CSS Grid, Flexbox, and mobile-first design principles. Create professional-grade user interfaces that adapt flawlessly across every screen size.
                </p>
                <div class="hero-buttons">
                    <a href="#features" class="btn-primary btn-large">Explore Features</a>
                    <a href="#contact" class="btn-secondary btn-large">Get Started</a>
                </div>
            </div>
            <div class="hero-image-container">
                <img src="https://images.unsplash.com/photo-1522071820081-009f0129c71c?w=700&auto=format&fit=crop&q=80" alt="Students collaborating on responsive web design" class="fluid-img">
            </div>
        </section>

        <!-- --- Features Section (CSS Grid Macro Layout) --- -->
        <section id="features" class="features-section">
            <div class="section-header">
                <h2>Core Development Pillars</h2>
                <p>Engineered using modern CSS layout standards and fluid responsive principles.</p>
            </div>

            <div class="features-grid">
                <!-- Feature Card 1 -->
                <article class="feature-card">
                    <div class="card-icon">📱</div>
                    <h3>Mobile-First Design</h3>
                    <p>Start with clean mobile baselines and progressively enhance layouts for larger tablet and desktop viewports.</p>
                </article>

                <!-- Feature Card 2 -->
                <article class="feature-card">
                    <div class="card-icon">📐</div>
                    <h3>CSS Grid & Flexbox</h3>
                    <p>Combine macro page structures in CSS Grid with micro component alignment using Flexbox.</p>
                </article>

                <!-- Feature Card 3 -->
                <article class="feature-card">
                    <div class="card-icon">⚡</div>
                    <h3>Fluid Typography</h3>
                    <p>Utilize `clamp()` and relative units to scale text and images proportionally without breaking constraints.</p>
                </article>
            </div>
        </section>

        <!-- --- Call-to-Action Banner --- -->
        <section id="contact" class="cta-banner">
            <div class="cta-box">
                <h2>Ready to Launch Your Web Development Career?</h2>
                <p>Join thousands of student developers building professional portfolios today.</p>
                <a href="#" class="btn-light btn-large">Join Our GitHub Organization</a>
            </div>
        </section>

    </main>

    <!-- --- Footer --- -->
    <footer class="site-footer">
        <div class="footer-container">
            <p>&copy; 2026 Tech Innovators Capstone. All rights reserved.</p>
            <ul class="footer-links">
                <li><a href="#">Privacy Policy</a></li>
                <li><a href="#">Terms of Service</a></li>
                <li><a href="#">GitHub Repo</a></li>
            </ul>
        </div>
    </footer>

</body>
</html>
File 2: landing-style.css (Mobile-First Stylesheet with Breakpoints)
CSS
/* --- Global Reset & Design Tokens --- */
:root {
    --primary-color: #0f172a;
    --accent-color: #2563eb;
    --bg-color: #f8fafc;
    --card-bg: #ffffff;
    --text-main: #334155;
    --text-muted: #64748b;
    --border-color: #e2e8f0;
}

* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    scroll-behavior: smooth;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: var(--bg-color);
    color: var(--text-main);
    line-height: 1.6;
    overflow-x: hidden; /* Prevents horizontal scroll overflow */
}

/* ==========================================================
   MOBILE-FIRST BASE STYLES (Small Screens / Mobile View)
   ========================================================== */

.site-header {
    background-color: var(--card-bg);
    border-bottom: 1px solid var(--border-color);
    position: sticky;
    top: 0;
    z-index: 1000;
}

.navbar {
    max-width: 1200px;
    margin: 0 auto;
    padding: 1rem 1.25rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 0.75rem;
}

.nav-logo a {
    font-size: 1.2rem;
    font-weight: 700;
    color: var(--primary-color);
    text-decoration: none;
}

/* Scrollable mobile nav links */
.nav-links {
    list-style: none;
    display: flex;
    gap: 1rem;
    overflow-x: auto;
    max-width: 100%;
    padding-bottom: 0.25rem;
}

.nav-links::-webkit-scrollbar {
    display: none; /* Hide scrollbar for clean UI */
}

.nav-links a {
    text-decoration: none;
    color: var(--text-muted);
    font-weight: 500;
    font-size: 0.9rem;
    white-space: nowrap;
    transition: color 0.2s ease;
}

.nav-links a:hover {
    color: var(--accent-color);
}

.nav-cta {
    display: none; /* Hidden on small mobile screens to save space */
}

/* --- Main Container --- */
.main-content {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 1.25rem;
}

/* --- Hero Section (Mobile Stacking) --- */
.hero-section {
    padding: 3rem 0;
    display: flex;
    flex-direction: column;
    gap: 2.5rem;
    text-align: center;
}

.hero-badge {
    display: inline-block;
    background-color: #dbeafe;
    color: #1e40af;
    font-size: 0.75rem;
    font-weight: 700;
    padding: 0.25rem 0.75rem;
    border-radius: 50px;
    text-transform: uppercase;
    margin-bottom: 1rem;
}

/* Fluid typography using clamp() */
.hero-text-content h1 {
    font-size: clamp(1.8rem, 5vw, 2.8rem);
    color: var(--primary-color);
    line-height: 1.25;
    margin-bottom: 1rem;
}

.hero-text-content p {
    font-size: 1rem;
    color: var(--text-muted);
    margin-bottom: 1.5rem;
}

.hero-buttons {
    display: flex;
    flex-direction: column;
    gap: 0.75rem;
}

.hero-image-container {
    width: 100%;
}

/* Fluid image constraints */
.fluid-img {
    width: 100%;
    height: auto;
    max-width: 500px;
    border-radius: 12px;
    box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.1);
    display: block;
    margin: 0 auto;
}

/* --- Features Section --- */
.features-section {
    padding: 3rem 0;
}

.section-header {
    text-align: center;
    margin-bottom: 2.5rem;
}

.section-header h2 {
    font-size: clamp(1.5rem, 3vw, 2.2rem);
    color: var(--primary-color);
    margin-bottom: 0.5rem;
}

.section-header p {
    color: var(--text-muted);
    font-size: 0.95rem;
}

/* CSS Grid with auto-fit for responsive cards */
.features-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 1.5rem;
}

.feature-card {
    background-color: var(--card-bg);
    border: 1px solid var(--border-color);
    border-radius: 10px;
    padding: 2rem 1.5rem;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.02);
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.feature-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.08);
}

.card-icon {
    font-size: 2rem;
    background-color: #f1f5f9;
    width: 50px;
    height: 50px;
    border-radius: 8px;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-bottom: 1.25rem;
}

.feature-card h3 {
    font-size: 1.15rem;
    color: var(--primary-color);
    margin-bottom: 0.5rem;
}

.feature-card p {
    font-size: 0.95rem;
    color: var(--text-muted);
}

/* --- Call-to-Action Banner --- */
.cta-banner {
    padding: 3rem 0 5rem 0;
}

.cta-box {
    background: linear-gradient(135deg, var(--primary-color), #1e3a8a);
    color: #ffffff;
    border-radius: 16px;
    padding: 3rem 1.5rem;
    text-align: center;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1.25rem;
}

.cta-box h2 {
    font-size: clamp(1.5rem, 3.5vw, 2.2rem);
}

.cta-box p {
    color: #cbd5e1;
    font-size: 1rem;
    max-width: 600px;
}

/* --- Shared Button Styles --- */
.btn-primary {
    background-color: var(--accent-color);
    color: #ffffff;
    font-weight: 600;
    text-decoration: none;
    padding: 0.6rem 1.25rem;
    border-radius: 6px;
    transition: background-color 0.2s ease;
    display: inline-block;
    text-align: center;
}

.btn-primary:hover {
    background-color: #1d4ed8;
}

.btn-secondary {
    background-color: #ffffff;
    color: var(--text-main);
    font-weight: 600;
    text-decoration: none;
    padding: 0.6rem 1.25rem;
    border: 1px solid var(--border-color);
    border-radius: 6px;
    transition: background-color 0.2s ease;
    display: inline-block;
    text-align: center;
}

.btn-secondary:hover {
    background-color: var(--bg-color);
}

.btn-light {
    background-color: #ffffff;
    color: var(--primary-color);
    font-weight: 600;
    text-decoration: none;
    padding: 0.75rem 1.75rem;
    border-radius: 6px;
    transition: background-color 0.2s ease;
    display: inline-block;
}

.btn-light:hover {
    background-color: #f1f5f9;
}

.btn-large {
    padding: 0.75rem 1.5rem;
    font-size: 0.95rem;
}

/* --- Footer --- */
.site-footer {
    background-color: var(--primary-color);
    color: #94a3b8;
    padding: 2.5rem 1.25rem;
    font-size: 0.9rem;
}

.footer-container {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1.25rem;
    text-align: center;
}

.footer-links {
    list-style: none;
    display: flex;
    gap: 1.5rem;
    flex-wrap: wrap;
    justify-content: center;
}

.footer-links a {
    color: #94a3b8;
    text-decoration: none;
    transition: color 0.2s ease;
}

.footer-links a:hover {
    color: #ffffff;
}


/* ==========================================================
   BREAKPOINT 1: TABLETS (min-width: 768px)
   ========================================================== */
@media (min-width: 768px) {
    .navbar {
        padding: 1rem 2rem;
    }

    .nav-cta {
        display: block; /* Reveal header CTA button on larger screens */
    }

    .main-content {
        padding: 0 2rem;
    }

    .hero-section {
        padding: 4rem 0;
    }

    .hero-buttons {
        flex-direction: row;
        justify-content: center;
    }

    .features-section, .cta-banner {
        padding: 4rem 0;
    }

    .cta-box {
        padding: 3.5rem 2.5rem;
    }

    .footer-container {
        flex-direction: row;
        justify-content: space-between;
        text-align: left;
    }
}


/* ==========================================================
   BREAKPOINT 2: DESKTOPS (min-width: 1024px)
   ========================================================== */
@media (min-width: 1024px) {
    .hero-section {
        flex-direction: row;            /* Side-by-side hero layout on desktop */
        align-items: center;
        justify-content: space-between;
        text-align: left;
        padding: 5rem 0;
        gap: 4rem;
    }

    .hero-text-content {
        flex: 1 1 500px;
    }

    .hero-buttons {
        justify-content: flex-start;
    }

    .hero-image-container {
        flex: 1 1 500px;
    }

    .fluid-img {
        max-width: 550px;
    }

    .site-footer {
        padding: 2.5rem 2rem;
    }
}