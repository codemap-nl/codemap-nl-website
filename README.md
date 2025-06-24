# CODEMAP Website

A collaborative platform connecting infectious disease modeling groups across the Netherlands

[![Website](https://img.shields.io/website?url=https%3A//codemap-nl.github.io/codemap-nl-website/)](https://codemap-nl.github.io/codemap-nl-website/)
[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)
[![Quarto](https://img.shields.io/badge/Made%20with-Quarto-blue)](https://quarto.org/)

## 🔬 About CODEMAP

CODEMAP (Collaborative Dutch Epidemic Modeling and Data Analytics Platform) is strengthening the field of infectious disease modelling and data analysis in the Netherlands in a sustainable way. Our platform connects 21 leading research institutions including universities, academic medical centers, research institutes, and government agencies.

### Reason for creating the platform
In 2023, in response to experiences gained during the COVID-19 pandemic, a symposium was organised on the future of infectious disease modelling and data analysis. Participants included staff from various national research institutes and academic groups, and all acknowledged the need for national collaboration. 

Based on recommendations from the international scientific audit on [COVID-19 data-analysis and modelling, in September 2023](https://www.rivm.nl/en/documenten/report-audit-rivm-covid-19-data-analytics-and-modelling-for-scientific-advice-to-policy-makers-2023), the Ministry of Health, Welfare and Sport (VWS) asked the National Institute for Public Health and the Environment (RIVM) to develop a roadmap for establishing a collaborative platform for infectious disease modelling and data analysis. This resulted in the creation of CODEMAP.

**🌐 Live Website:** <https://codemap-nl.github.io/codemap-nl-website/>

## 🏛️ Partner Organizations

Our collaborative network includes:

- **10 Universities** - Leading academic institutions across the Netherlands
- **5 Medical Centers** - Academic medical centers advancing clinical research
- **6 Research Institutes & Government Agencies** - National and international research organizations

[View all partners →](https://codemap-nl.github.io/codemap-nl-website/members/)

## 🛠️ Technical Stack

This website is built with modern web technologies:

- [**Quarto**](https://quarto.org/) - Scientific and technical publishing system
- **HTML5/CSS3** - Modern web standards with custom styling
- **JavaScript** - Interactive features and animations
- **GitHub Pages** - Automated deployment and hosting
- **GitHub Actions** - Continuous integration and deployment

## 📁 Repository Structure

```
codemap-nl-website/
├── _quarto.yml              # Quarto project configuration
├── index.qmd                # Homepage
├── about.qmd                # About page
├── members/                 # Partner organizations
│   └── index.qmd
├── events/                  # Events and workshops
│   └── index.qmd
├── resources/               # Learning resources
│   └── index.qmd
├── news/                    # News and updates
│   └── index.qmd
├── _includes/               # Shared components
│   ├── styles.css          # Custom CSS styling
│   └── scripts.html        # Interactive JavaScript
├── images/                  # Image assets
│   ├── logos/              # Organization logos
│   └── favicon.ico
├── docs/                    # Generated site (GitHub Pages)
└── .github/
    └── workflows/
        └── publish.yml      # GitHub Actions deployment
```

## 🚀 Getting Started

### Prerequisites

- [Quarto](https://quarto.org/docs/get-started/) installed
- [Git](https://git-scm.com/) for version control
- A web browser

### Local Development

1. **Clone the repository:**
   ```bash
   git clone https://github.com/codemap-nl/codemap-nl-website.git
   cd codemap-nl-website
   ```

2. **Preview the site:**
   ```bash
   quarto preview
   ```
   The site will be available at `http://localhost:4200`

3. **Build the site:**
   ```bash
   quarto render
   ```

### Making Changes

1. **Edit content** in `.qmd` files using Markdown syntax
2. **Update styling** in `_includes/styles.css`
3. **Add images** to the `images/` directory
4. **Test locally** with `quarto preview`
5. **Commit and push** changes to trigger automatic deployment

## 🎨 Customization

### Adding New Pages

1. Create a new `.qmd` file
2. Add YAML front matter:
   ```yaml
   ---
   title: "Page Title"
   subtitle: "Page subtitle"
   ---
   ```
3. Add the page to `_quarto.yml` navigation

### Updating Partner Logos

1. Add logo files to `images/logos/`
2. Update `members/index.qmd` with new logo and link
3. Recommended logo specs:
   - Format: PNG with transparent background
   - Size: 200px wide maximum
   - File size: Under 20KB

### Styling

The website uses a custom CSS framework with:

- **CSS Custom Properties** for consistent theming
- **Responsive Grid System** for layouts
- **Modern CSS Features** (backdrop-filter, animations)
- **Accessibility-first design** patterns

Key CSS classes:

- `.hero-section` - Landing page hero
- `.logo-grid` - Partner organization displays
- `.stats-section` - Statistics and metrics
- `.btn-primary` - Call-to-action buttons

## 🔄 Deployment

The website automatically deploys to GitHub Pages when changes are pushed to the `main` branch using GitHub Actions.

### Manual Deployment

```bash
# Render the site
quarto render

# The site will be built to the docs/ directory
# GitHub Pages serves from this directory
```

### Deployment Workflow

1. **Push to main** - Triggers GitHub Actions
2. **Quarto renders** - Builds the site
3. **Deploy to Pages** - Site goes live automatically
4. **Available at** - https://codemap-nl.github.io/codemap-nl-website/

## 🤝 Contributing

We welcome contributions from the CODEMAP community!

### How to Contribute

1. **Fork** the repository
2. **Create a feature branch:** `git checkout -b feature/new-feature`
3. **Make your changes** and test locally
4. **Commit:** `git commit -m "Add new feature"`
5. **Push:** `git push origin feature/new-feature`
6. **Create a Pull Request**

### Contribution Guidelines

- **Content updates** - Partner information, events, resources
- **Bug fixes** - Layout issues, broken links, typos
- **Feature additions** - New pages, improved functionality
- **Design improvements** - Better accessibility, mobile responsiveness

### Reporting Issues

Found a bug or have a suggestion? [Open an issue](https://github.com/codemap-nl/codemap-nl-website/issues) with:

- Clear description of the problem
- Steps to reproduce (if applicable)
- Screenshots (if relevant)
- Suggested solution

## 📄 License

This project is licensed under the [Creative Commons Attribution-NonCommercial 4.0 International License](https://creativecommons.org/licenses/by-nc/4.0/).

**You are free to:**

- **Share** - Copy and redistribute the material
- **Adapt** - Remix, transform, and build upon the material

**Under the following terms:**

- **Attribution** - Give appropriate credit
- **NonCommercial** - Not for commercial purposes

## 📞 Contact

- **Email:** [collabforepidemodatanalytics@rivm.nl](mailto:collabforepidemodatanalytics@rivm.nl)
- **Website:** [RIVM Collaborative Platform](https://codemap-nl.github.io/codemap-nl-website/)
- **LinkedIn:** [CODEMAP Group](https://www.linkedin.com/groups/13094435/)
- **GitHub:** [codemap-nl](https://github.com/codemap-nl)

---

<div align="center">

[**🌐 Visit Website**](https://codemap-nl.github.io/codemap-nl-website/) **|** [**👥 View Partners**](https://codemap-nl.github.io/codemap-nl-website/members/) **|** [**📧 Contact Us**](mailto:collabforepidemodatanalytics@rivm.nl)

*Built with ❤️ by the CODEMAP community*

</div>
