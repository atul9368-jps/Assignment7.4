The HTML File (index.html)
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Modern Landing Page - Header & Hero</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Steps 1 & 6: Sticky Navigation Header -->
    <header class="site-header">
        <div class="nav-container">
            <div class="logo">SaaSify</div>
            <nav class="nav-links">
                <a href="#features">Features</a>
                <a href="#solutions">Solutions</a>
                <a href="#pricing">Pricing</a>
                <a href="#about">About</a>
            </nav>
            <div class="nav-action">
                <a href="#get-started" class="btn btn-secondary">Get Started</a>
            </div>
        </div>
    </header>

    <!-- Steps 2, 3, 4, & 5: Hero Section -->
    <main class="hero-section">
        <div class="hero-container">
            
            <!-- Hero Text Content -->
            <div class="hero-content">
                <h1>Build Better Products Faster</h1>
                <p>Empower your team with a modern platform designed to streamline workflows, boost collaboration, and scale your business effortlessly.</p>
                <div class="hero-buttons">
                    <a href="#signup" class="btn btn-primary">Start Free Trial</a>
                    <a href="#demo" class="btn btn-outline">Watch Demo</a>
                </div>
            </div>

            <!-- Hero Image / Illustration -->
            <div class="hero-image">
                <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?auto=format&fit=crop&q=80&w=600" alt="Dashboard Illustration">
            </div>

        </div>
    </main>

    <!-- Step 6: Styled Footer Section -->
    <footer class="site-footer">
        <div class="footer-container">
            <p>&copy; 2026 SaaSify Inc. All rights reserved.</p>
            <div class="footer-links">
                <a href="#privacy">Privacy Policy</a>
                <a href="#terms">Terms of Service</a>
            </div>
        </div>
    </footer>

</body>
</html>
2. The CSS File (style.css)
CSS
/* Global Reset & Typography */
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
    background-color: #f8fafc;
    color: #1e293b;
    line-height: 1.6;
    display: flex;
    flex-direction: column;
    min-height: 100vh;
}

/* Step 1 & 6: Sticky Header */
.site-header {
    position: sticky;
    top: 0;
    background-color: #ffffff;
    border-bottom: 1px solid #e2e8f0;
    z-index: 1000;
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
}

.nav-container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 16px 24px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.logo {
    font-size: 1.5rem;
    font-weight: 800;
    color: #2563eb;
    letter-spacing: -0.5px;
}

.nav-links {
    display: flex;
    gap: 32px;
}

.nav-links a {
    text-decoration: none;
    color: #64748b;
    font-weight: 600;
    font-size: 0.95rem;
    transition: color 0.2s ease;
}

.nav-links a:hover {
    color: #2563eb;
}

/* Steps 2, 3, 4, & 5: Hero Section & Flexbox Layout */
.hero-section {
    flex: 1;
    display: flex;
    align-items: center;
    padding: 80px 24px;
}

.hero-container {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 60px;
    flex-wrap: wrap; /* Step 7: Allows wrapping on smaller viewports */
}

.hero-content {
    flex: 1;
    min-width: 300px;
}

.hero-content h1 {
    font-size: 3rem;
    font-weight: 800;
    color: #0f172a;
    line-height: 1.2;
    margin-bottom: 20px;
}

.hero-content p {
    font-size: 1.15rem;
    color: #64748b;
    margin-bottom: 30px;
    max-width: 500px;
}

.hero-buttons {
    display: flex;
    gap: 16px;
    flex-wrap: wrap;
}

.hero-image {
    flex: 1;
    min-width: 300px;
    text-align: center;
}

.hero-image img {
    width: 100%;
    max-width: 550px;
    height: auto;
    border-radius: 12px;
    box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
}

/* Button Styles */
.btn {
    display: inline-block;
    padding: 12px 24px;
    border-radius: 6px;
    font-weight: 600;
    text-decoration: none;
    transition: background-color 0.2s ease, transform 0.1s ease;
}

.btn:active {
    transform: scale(0.98);
}

.btn-primary {
    background-color: #2563eb;
    color: #ffffff;
}

.btn-primary:hover {
    background-color: #1d4ed8;
}

.btn-secondary {
    background-color: #eff6ff;
    color: #2563eb;
    padding: 10px 20px;
}

.btn-secondary:hover {
    background-color: #dbeafe;
}

.btn-outline {
    background-color: transparent;
    color: #334155;
    border: 1px solid #cbd5e1;
}

.btn-outline:hover {
    background-color: #f1f5f9;
}

/* Step 6: Styled Footer */
.site-footer {
    background-color: #ffffff;
    border-top: 1px solid #e2e8f0;
    padding: 24px;
}

.footer-container {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 16px;
    font-size: 0.875rem;
    color: #64748b;
}

.footer-links {
    display: flex;
    gap: 20px;
}

.footer-links a {
    text-decoration: none;
    color: #64748b;
    transition: color 0.2s;
}

.footer-links a:hover {
    color: #2563eb;
}

/* Step 7: Responsive Media Query */
@media (max-width: 768px) {
    .nav-links {
        display: none; /* Collapses navigation links for smaller mobile screens */
    }
    .hero-content h1 {
        font-size: 2.25rem;
    }
    .hero-container {
        justify-content: center;
        text-align: center;
    }
    .hero-content p {
        margin: 0 auto 30px auto;
    }
    .hero-buttons {
        justify-content: center;
    }
}