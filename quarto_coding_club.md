---
title: "Coding Club"
subtitle: "Everybody can learn to code"
page-layout: custom
toc: false
---

```{=html}
<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap');

:root {
    --primary-color: #2563eb;
    --secondary-color: #667eea;
    --accent-color: #764ba2;
    --text-dark: #1e293b;
    --text-light: #64748b;
    --background-light: #f8fafc;
}

body {
    font-family: 'Inter', sans-serif;
    line-height: 1.6;
    color: var(--text-dark);
    margin: 0;
    padding: 0;
}

/* Hero Section */
.hero-section {
    min-height: 90vh;
    background: linear-gradient(135deg, var(--secondary-color) 0%, var(--accent-color) 100%);
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    color: white;
    position: relative;
    overflow: hidden;
    margin: 0;
    padding: 2rem;
}

.hero-section::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="grid" width="10" height="10" patternUnits="userSpaceOnUse"><path d="M 10 0 L 0 0 0 10" fill="none" stroke="rgba(255,255,255,0.1)" stroke-width="0.5"/></pattern></defs><rect width="100" height="100" fill="url(%23grid)"/></svg>');
    opacity: 0.3;
}

.hero-content {
    z-index: 2;
    max-width: 800px;
}

.hero-title {
    font-size: 4rem;
    font-weight: 700;
    margin-bottom: 1rem;
    animation: fadeInUp 1s ease forwards;
}

.hero-subtitle {
    font-size: 1.5rem;
    font-weight: 300;
    margin-bottom: 2rem;
    animation: fadeInUp 1s ease 0.2s both;
}

.hero-description {
    font-size: 1.1rem;
    margin-bottom: 3rem;
    animation: fadeInUp 1s ease 0.4s both;
    opacity: 0.9;
}

.cta-button {
    display: inline-block;
    background: rgba(255, 255, 255, 0.2);
    color: white;
    padding: 1rem 2rem;
    text-decoration: none;
    border-radius: 50px;
    font-weight: 600;
    backdrop-filter: blur(10px);
    border: 2px solid rgba(255, 255, 255, 0.3);
    transition: all 0.3s ease;
    animation: fadeInUp 1s ease 0.6s both;
}

.cta-button:hover {
    background: rgba(255, 255, 255, 0.3);
    transform: translateY(-2px);
    color: white;
    text-decoration: none;
}

/* Quote Section */
.quote-section {
    background: linear-gradient(135deg, #1e3a8a 0%, #3730a3 100%);
    padding: 6rem 2rem;
    text-align: center;
    color: white;
    margin: 0;
}

.quote-text {
    font-size: 2rem;
    font-weight: 300;
    line-height: 1.4;
    margin-bottom: 2rem;
    max-width: 900px;
    margin-left: auto;
    margin-right: auto;
}

.quote-logo {
    width: 80px;
    height: 80px;
    background: rgba(255, 255, 255, 0.1);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 2rem auto 0;
    font-size: 2rem;
}

/* Cards Section */
.cards-section {
    padding: 6rem 2rem;
    background: var(--background-light);
    margin: 0;
}

.section-title {
    text-align: center;
    font-size: 2.5rem;
    font-weight: 600;
    margin-bottom: 3rem;
    color: var(--text-dark);
}

.cards-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
    max-width: 1200px;
    margin: 0 auto;
}

.feature-card {
    background: white;
    border-radius: 20px;
    overflow: hidden;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
    transition: all 0.3s ease;
    cursor: pointer;
}

.feature-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
}

.card-header {
    height: 200px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    font-size: 3rem;
    position: relative;
}

.card-header.team { background: linear-gradient(45deg, #667eea, #764ba2); }
.card-header.skills { background: linear-gradient(45deg, #276dc3, #165ba8); }
.card-header.resources { background: linear-gradient(45deg, #ff6b6b, #4ecdc4); }
.card-header.events { background: linear-gradient(45deg, #f7df1e, #323330); color: #323330; }

.card-content {
    padding: 2rem;
}

.card-title {
    font-size: 1.3rem;
    font-weight: 600;
    margin-bottom: 1rem;
    color: var(--text-dark);
}

.card-description {
    color: var(--text-light);
    line-height: 1.6;
    margin-bottom: 1.5rem;
}

.card-dots {
    display: flex;
    gap: 0.5rem;
}

.dot {
    width: 8px;
    height: 8px;
    background: #e2e8f0;
    border-radius: 50%;
    animation: pulse 2s infinite;
}

.dot:nth-child(2) { animation-delay: 0.2s; }
.dot:nth-child(3) { animation-delay: 0.4s; }

/* Resources Grid */
.resources-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 1.5rem;
    margin: 3rem 0;
    max-width: 1000px;
    margin-left: auto;
    margin-right: auto;
}

.resource-item {
    background: white;
    padding: 1.5rem;
    border-radius: 12px;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease;
    text-align: center;
}

.resource-item:hover {
    transform: translateY(-5px);
}

.resource-icon {
    font-size: 2.5rem;
    margin-bottom: 1rem;
    color: var(--primary-color);
}

.resource-title {
    font-weight: 600;
    margin-bottom: 0.5rem;
    color: var(--text-dark);
}

.resource-description {
    color: var(--text-light);
    font-size: 0.9rem;
}

/* Animations */
@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translateY(30px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

@keyframes pulse {
    0%, 100% {
        opacity: 0.4;
        transform: scale(1);
    }
    50% {
        opacity: 1;
        transform: scale(1.2);
    }
}

/* Mobile Responsiveness */
@media (max-width: 768px) {
    .hero-title {
        font-size: 2.5rem;
    }
    
    .hero-subtitle {
        font-size: 1.2rem;
    }
    
    .quote-text {
        font-size: 1.5rem;
    }
    
    .cards-grid {
        grid-template-columns: 1fr;
    }
    
    .hero-section, .quote-section, .cards-section {
        padding: 3rem 1rem;
    }
}

/* Footer */
.footer {
    background: var(--text-dark);
    color: white;
    padding: 3rem 2rem 2rem;
    margin: 0;
}

.footer-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 2rem;
    max-width: 1200px;
    margin: 0 auto;
}

.footer-section h4 {
    font-size: 1.2rem;
    font-weight: 600;
    margin-bottom: 1rem;
}

.footer-section p,
.footer-section a {
    color: #94a3b8;
    text-decoration: none;
    line-height: 1.8;
    margin-bottom: 0.5rem;
    display: block;
}

.footer-section a:hover {
    color: white;
}

.footer-bottom {
    text-align: center;
    margin-top: 2rem;
    padding-top: 2rem;
    border-top: 1px solid #334155;
    color: #64748b;
}
</style>
```

::: {.hero-section}
::: {.hero-content}
# We are the<br>Coding Club {.hero-title}

Everybody can learn to code {.hero-subtitle}

Founded with the belief that coding is amazing, meaningful, well-rewarded, and easy to learn. We provide our community with a platform for learning and developing coding skills for multiple purposes. {.hero-description}

[Join Our Community](#about){.cta-button}
:::
:::

::: {.quote-section}
Our goal as a club is to help everyone learn coding skills and show that coding is for everyone, no matter our background. {.quote-text}

::: {.quote-logo}
💻
:::
:::

::: {.cards-section #about}
## What We Offer {.section-title}

::: {.cards-grid}
::: {.feature-card}
::: {.card-header .team}
👥
:::
::: {.card-content}
### Who are we? {.card-title}
We are a group of enthusiastic students who are passionate about coding and data science, building a community of learners. {.card-description}

::: {.card-dots}
::: {.dot}
:::
::: {.dot}
:::
::: {.dot}
:::
:::
:::
:::

::: {.feature-card}
::: {.card-header .skills}
📊
:::
::: {.card-content}
### Boost your skills {.card-title}
Develop your coding skills in R, Python, and other languages for data analysis, visualization, and beyond. {.card-description}

::: {.card-dots}
::: {.dot}
:::
::: {.dot}
:::
::: {.dot}
:::
:::
:::
:::

::: {.feature-card}
::: {.card-header .resources}
🎓
:::
::: {.card-content}
### Certifications & Resources {.card-title}
Get free access to our materials, books, and resources to boost your coding skills and earn certifications. {.card-description}

::: {.card-dots}
::: {.dot}
:::
::: {.dot}
:::
::: {.dot}
:::
:::
:::
:::

::: {.feature-card}
::: {.card-header .events}
📅
:::
::: {.card-content}
### Events & Workshops {.card-title}
Check our past and upcoming events, workshops, and coding sessions designed to enhance your learning experience. {.card-description}

::: {.card-dots}
::: {.dot}
:::
::: {.dot}
:::
::: {.dot}
:::
:::
:::
:::
:::
:::

## Learning Resources {.section-title}

::: {.resources-grid}
::: {.resource-item}
::: {.resource-icon}
🐍
:::
::: {.resource-title}
Python Programming
:::
::: {.resource-description}
Learn Python from basics to advanced data science applications
:::
:::

::: {.resource-item}
::: {.resource-icon}
📈
:::
::: {.resource-title}
R for Data Science
:::
::: {.resource-description}
Master statistical analysis and visualization with R
:::
:::

::: {.resource-item}
::: {.resource-icon}
🌐
:::
::: {.resource-title}
Web Development
:::
::: {.resource-description}
Build modern websites with HTML, CSS, and JavaScript
:::
:::

::: {.resource-item}
::: {.resource-icon}
🤖
:::
::: {.resource-title}
Machine Learning
:::
::: {.resource-description}
Explore AI and ML algorithms for real-world applications
:::
:::
:::

::: {.footer}
::: {.footer-grid}
::: {.footer-section}
#### About Coding Club
We believe coding is for everyone. Join our community and start your coding journey today with supportive peers and comprehensive resources.
:::

::: {.footer-section}
#### Quick Links
[Learn to Code](#learn)
[Upcoming Events](#events)
[Free Resources](#resources)
[Get in Touch](#contact)
:::

::: {.footer-section}
#### Languages & Tools
[Python Tutorials](#python)
[R Programming](#r)
[Data Science](#datascience)
[Web Development](#webdev)
:::

::: {.footer-section}
#### Connect
[📧 Email](mailto:contact@codingclub.com)
[💬 Discord](#discord)
[🐙 GitHub](#github)
[📱 Twitter](#twitter)
:::
:::

::: {.footer-bottom}
© 2025 Coding Club. Licensed under Creative Commons Attribution-NonCommercial 4.0 International License.
:::
:::

```{=html}
<script>
// Smooth scrolling for anchor links
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function (e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        if (target) {
            target.scrollIntoView({
                behavior: 'smooth',
                block: 'start'
            });
        }
    });
});

// Add scroll animations
const observerOptions = {
    threshold: 0.1,
    rootMargin: '0px 0px -50px 0px'
};

const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
        if (entry.isIntersecting) {
            entry.target.style.opacity = '1';
            entry.target.style.transform = 'translateY(0)';
        }
    });
}, observerOptions);

// Observe cards for animation
document.querySelectorAll('.feature-card, .resource-item').forEach(card => {
    card.style.opacity = '0';
    card.style.transform = 'translateY(30px)';
    card.style.transition = 'all 0.6s ease';
    observer.observe(card);
});

// Enhanced card interactions
document.querySelectorAll('.feature-card, .resource-item').forEach(card => {
    card.addEventListener('mouseenter', () => {
        card.style.transform = 'translateY(-15px) scale(1.02)';
    });
    
    card.addEventListener('mouseleave', () => {
        card.style.transform = 'translateY(0) scale(1)';
    });
});
</script>
```