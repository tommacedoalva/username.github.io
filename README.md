/* ============================================
   QUINCEAÑERA INVITATION - CELESTIAL THEME
   Colors: Royal Blue, Gold, Silver
   ============================================ */

/* CSS Variables */
:root {
    /* Primary Colors - Royal Blue */
    --primary-500: #0A4DAA;
    --primary-700: #07387D;
    --primary-900: #052654;
    
    /* Neutral - Night & Starlight */
    --bg-page: #031022;
    --bg-surface: #0F213A;
    --text-primary: #E2E8F0;
    --text-secondary: #94A3B8;
    
    /* Accent - Metallic */
    --accent-gold: #E2B870;
    --accent-silver: #C0C0C0;
    
    /* Spacing */
    --spacing-xs: 8px;
    --spacing-sm: 16px;
    --spacing-md: 24px;
    --spacing-lg: 48px;
    --spacing-xl: 64px;
    --spacing-xxl: 96px;
    
    /* Radius */
    --radius-md: 12px;
    --radius-lg: 16px;
    
    /* Typography */
    --font-heading: 'Lora', serif;
    --font-body: 'Inter', sans-serif;
}

/* Reset & Base Styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: var(--font-body);
    background: var(--bg-page);
    color: var(--text-primary);
    overflow-x: hidden;
    position: relative;
    line-height: 1.7;
}

/* Starfield Canvas Background */
#starfield {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: 0;
    pointer-events: none;
}

/* Hero Section */
.hero {
    position: relative;
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    overflow: hidden;
    z-index: 1;
}

.moon {
    position: absolute;
    width: 400px;
    height: 400px;
    border-radius: 50%;
    background: radial-gradient(circle at 30% 30%, #E8E8E8, #B0B0B0, #808080);
    box-shadow: 
        0 0 80px rgba(226, 184, 112, 0.3),
        0 0 120px rgba(10, 77, 170, 0.2),
        inset -30px -30px 60px rgba(0, 0, 0, 0.2);
    top: 15%;
    left: 50%;
    transform: translateX(-50%);
    z-index: -1;
    opacity: 0.8;
    animation: moonFloat 20s ease-in-out infinite;
}

@keyframes moonFloat {
    0%, 100% { transform: translateX(-50%) translateY(0px); }
    50% { transform: translateX(-50%) translateY(-30px); }
}

.hero-content {
    position: relative;
    z-index: 2;
    padding: var(--spacing-md);
}

.subtitle {
    font-family: var(--font-body);
    font-size: 18px;
    color: var(--text-secondary);
    letter-spacing: 2px;
    text-transform: uppercase;
    margin-bottom: var(--spacing-md);
}

.names {
    font-family: var(--font-heading);
    font-size: 56px;
    font-weight: 600;
    color: var(--accent-gold);
    letter-spacing: -1px;
    line-height: 1.2;
    margin-bottom: var(--spacing-sm);
    text-shadow: 0 0 30px rgba(226, 184, 112, 0.5);
}

.lastname {
    font-family: var(--font-heading);
    font-size: 32px;
    font-weight: 600;
    color: var(--text-primary);
    letter-spacing: -0.5px;
    line-height: 1.3;
}

.scroll-indicator {
    margin-top: var(--spacing-xl);
    color: var(--accent-silver);
    animation: bounce 2s ease-in-out infinite;
}

@keyframes bounce {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(10px); }
}

/* Container */
.container {
    position: relative;
    z-index: 1;
    max-width: 800px;
    margin: 0 auto;
    padding: var(--spacing-md);
}

/* Card Styles */
.card {
    background: var(--bg-surface);
    border-radius: var(--radius-md);
    padding: var(--spacing-lg);
    margin-bottom: var(--spacing-xxl);
    box-shadow: 0 0 32px rgba(10, 77, 170, 0.2);
    text-align: center;
    position: relative;
}

/* Star Decoration */
.star-decoration {
    position: absolute;
    top: -20px;
    left: 50%;
    transform: translateX(-50%);
    animation: twinkle 3s ease-in-out infinite;
}

@keyframes twinkle {
    0%, 100% { opacity: 1; transform: translateX(-50%) scale(1); }
    50% { opacity: 0.6; transform: translateX(-50%) scale(1.1); }
}

/* Event Details */
.event-details {
    padding-top: var(--spacing-xl);
}

.date-section {
    margin-bottom: var(--spacing-md);
}

.date-label {
    font-family: var(--font-body);
    font-size: 18px;
    color: var(--text-secondary);
    text-transform: uppercase;
    letter-spacing: 2px;
    margin-bottom: var(--spacing-xs);
}

.date-main {
    font-family: var(--font-heading);
    font-size: 48px;
    font-weight: 600;
    color: var(--text-primary);
    line-height: 1.2;
}

.date-year {
    font-family: var(--font-heading);
    font-size: 24px;
    color: var(--accent-gold);
    margin-top: var(--spacing-xs);
}

.divider {
    width: 100px;
    height: 2px;
    background: linear-gradient(to right, transparent, var(--accent-gold), var(--accent-silver), transparent);
    margin: var(--spacing-lg) auto;
}

.time-section,
.venue-section {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: var(--spacing-sm);
    margin-bottom: var(--spacing-md);
}

.icon {
    color: var(--accent-gold);
    flex-shrink: 0;
}

.time {
    font-family: var(--font-body);
    font-size: 20px;
    color: var(--text-secondary);
}

.venue-text {
    text-align: left;
}

.venue-address {
    font-family: var(--font-heading);
    font-size: 24px;
    color: var(--text-primary);
    margin-bottom: var(--spacing-xs);
}

.venue-reference {
    font-size: 16px;
    color: var(--text-secondary);
}

/* Family Section */
.family-section {
    padding: var(--spacing-xl);
}

.section-title {
    font-family: var(--font-heading);
    font-size: 32px;
    font-weight: 600;
    color: var(--accent-gold);
    margin-bottom: var(--spacing-lg);
    letter-spacing: -0.5px;
}

.family-group {
    margin-bottom: var(--spacing-lg);
}

.family-subtitle {
    font-family: var(--font-heading);
    font-size: 20px;
    font-weight: 500;
    color: var(--text-secondary);
    margin-bottom: var(--spacing-md);
    text-transform: uppercase;
    letter-spacing: 1px;
}

.family-name {
    font-family: var(--font-body);
    font-size: 18px;
    color: var(--text-primary);
    margin-bottom: var(--spacing-xs);
}

.star-cluster {
    display: flex;
    justify-content: center;
    margin: var(--spacing-lg) 0;
}

/* Confirmation Section */
.confirmation-section {
    text-align: center;
    margin-bottom: var(--spacing-xxl);
}

.confirmation-text {
    font-size: 18px;
    color: var(--text-secondary);
    margin-bottom: var(--spacing-lg);
}

.cta-button {
    display: inline-flex;
    align-items: center;
    gap: var(--spacing-sm);
    height: 56px;
    padding: 0 32px;
    background: var(--accent-gold);
    color: var(--bg-page);
    font-family: var(--font-body);
    font-size: 18px;
    font-weight: 500;
    text-decoration: none;
    border-radius: var(--radius-lg);
    transition: all 300ms cubic-bezier(0.25, 0.8, 0.25, 1);
    box-shadow: 0 0 24px rgba(226, 184, 112, 0.4);
}

.cta-button:hover {
    transform: translateY(-4px);
    box-shadow: 0 8px 32px rgba(226, 184, 112, 0.6);
}

.cta-button:active {
    transform: translateY(-2px);
}

/* Footer */
.footer {
    text-align: center;
    padding: var(--spacing-xl) var(--spacing-md);
}

.sparkles {
    display: flex;
    justify-content: center;
    margin-bottom: var(--spacing-md);
}

.footer-text {
    font-family: var(--font-heading);
    font-size: 18px;
    color: var(--text-secondary);
}

/* Fade-in Animations */
.fade-in {
    animation: fadeIn 1200ms ease-out forwards;
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

.fade-in-scroll {
    opacity: 0;
    transform: translateY(30px);
    transition: opacity 800ms ease-out, transform 800ms ease-out;
}

.fade-in-scroll.visible {
    opacity: 1;
    transform: translateY(0);
}

/* Responsive Design - Mobile */
@media (max-width: 768px) {
    :root {
        --spacing-xxl: 64px;
    }
    
    .names {
        font-size: 40px;
    }
    
    .lastname {
        font-size: 28px;
    }
    
    .subtitle {
        font-size: 16px;
    }
    
    .moon {
        width: 250px;
        height: 250px;
    }
    
    .card {
        padding: var(--spacing-md);
    }
    
    .event-details {
        padding-top: var(--spacing-lg);
    }
    
    .date-main {
        font-size: 36px;
    }
    
    .date-year {
        font-size: 20px;
    }
    
    .venue-address {
        font-size: 20px;
    }
    
    .section-title {
        font-size: 28px;
    }
    
    .time-section,
    .venue-section {
        flex-direction: column;
        text-align: center;
    }
    
    .venue-text {
        text-align: center;
    }
}

/* Accessibility - Reduced Motion */
@media (prefers-reduced-motion: reduce) {
    * {
        animation-duration: 0.01ms !important;
        animation-iteration-count: 1 !important;
        transition-duration: 0.01ms !important;
    }
    
    .moon {
        animation: none;
    }
}
