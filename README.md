# 📚 Project Catalog

> A beautiful, automated documentation website showcasing all my GitHub projects, built with MkDocs and deployed to GitHub Pages.

**Live Site:** [https://ly2xxx.github.io/catalog](https://ly2xxx.github.io/catalog)

## 🌟 Overview

This project automatically catalogs all my public repositories into a searchable, organized documentation website. It features modern Material Design, automatic categorization, and seamless GitHub integration.

### ✨ Features

- **🤖 Automated Documentation** - GitHub Actions automatically deploys updates
- **📱 Responsive Design** - Works perfectly on desktop and mobile  
- **🔍 Full-Text Search** - Find any project instantly
- **🎨 Material Design** - Beautiful, modern interface with dark/light mode
- **📊 Project Metrics** - Stars, forks, and activity indicators
- **🏷️ Smart Categorization** - Projects organized by technology and purpose
- **⚡ Fast Loading** - Optimized for speed and performance

### 🗂️ Current Categories

- **🤖 AI & Machine Learning** - LangGraph agents, RAG systems, computer vision
- **🛠️ Development Tools** - CLI utilities, DevOps tools, automation scripts  
- **🌐 Web Applications** - Full-stack apps, APIs, frontend projects
- **📚 Learning & Tutorials** - Educational content, labs, experiments
- **🔬 Proof of Concepts** - Early-stage ideas, technical prototypes

---

## 🚀 Quick Start

### Prerequisites

- Python 3.8+
- Git

### Local Development

```bash
# Clone the repository
git clone https://github.com/ly2xxx/catalog.git
cd catalog

# Install dependencies
pip install -r requirements.txt

# Start development server
mkdocs serve

# Open browser to http://localhost:8000
```

### Building for Production

```bash
# Build static site
mkdocs build

# Deploy to GitHub Pages
mkdocs gh-deploy
```

---

## 📈 Expanding the Catalog

### Adding New Projects

#### 1. Automatic Detection
New public repositories are automatically detected when you update the catalog content. The system is designed to be flexible and accommodate new projects.

#### 2. Manual Addition Process

**Step 1: Identify the Category**
Determine which category your new project belongs to:
- `ai-ml.md` - AI/ML projects, agents, RAG systems
- `dev-tools.md` - CLI tools, DevOps utilities, frameworks
- `web-apps.md` - Web applications, APIs, frontend projects  
- `learning.md` - Tutorials, educational content, labs
- `poc.md` - Proof of concepts, experimental projects

**Step 2: Edit the Category File**
Navigate to `docs/projects/[category].md` and add your project:

```markdown
### [project-name](https://github.com/ly2xxx/project-name)
**Brief Description**

Detailed description of what the project does and why it's interesting.

- **Tech Stack:** Technology, Frameworks, Languages
- **Features:** Key features and capabilities
- **Status:** Development stage (Active, Beta, Stable, etc.)
- **Stars:** ⭐ X | **Forks:** 🍴 Y
- **License:** MIT/Apache/etc (if applicable)

---
```

**Step 3: Update Navigation (if needed)**
If adding a new category, update `mkdocs.yml`:

```yaml
nav:
  - Home: index.md
  - Projects:
    - AI & Machine Learning: projects/ai-ml.md
    - Development Tools: projects/dev-tools.md
    - Web Applications: projects/web-apps.md
    - Learning & Tutorials: projects/learning.md
    - Proof of Concepts: projects/poc.md
    - Your New Category: projects/new-category.md  # Add here
  - About: about.md
  - Contributing: contributing.md
```

### Creating New Categories

#### When to Create a New Category
- When you have 3+ projects that don't fit existing categories
- When a specific technology domain becomes prominent (e.g., "Mobile Apps", "Data Science")
- When you want to highlight a particular focus area

#### How to Create a New Category

**Step 1: Create the Documentation File**
```bash
# Create new category file
touch docs/projects/new-category.md
```

**Step 2: Use the Category Template**
```markdown
# 🏷️ New Category Name

Brief description of what projects belong in this category.

## 🚀 Featured Projects

### [project-name](https://github.com/ly2xxx/project-name)
**Project Description**

Project details...

- **Tech Stack:** Technologies used
- **Features:** Key capabilities  
- **Status:** Current state
- **Stars:** ⭐ X

---

## 📊 Key Technologies

=== "Primary Tech"
    
    - **Technology 1** - Description
    - **Technology 2** - Description

=== "Secondary Tech"
    
    - **Tool 1** - Usage
    - **Tool 2** - Usage

## 🔗 Related Projects

- [Link to related project 1](https://github.com/ly2xxx/related1)
- [Link to related project 2](https://github.com/ly2xxx/related2)

---

*Category-specific notes or guidelines*
```

**Step 3: Update Configuration**
Add to `mkdocs.yml` navigation section and update the home page.

### Automation Opportunities

#### 1. GitHub API Integration
Create a Python script to automatically fetch repository data:

```python
# scripts/update_catalog.py
import requests
import json
from datetime import datetime

def fetch_repositories(username):
    """Fetch all public repositories for a user"""
    url = f"https://api.github.com/users/{username}/repos"
    response = requests.get(url)
    return response.json()

def categorize_project(repo):
    """Auto-categorize based on language, topics, and description"""
    language = repo.get('language', '').lower()
    topics = repo.get('topics', [])
    description = repo.get('description', '').lower()
    
    # AI/ML keywords
    ai_keywords = ['ai', 'ml', 'langchain', 'langraph', 'rag', 'llm']
    if any(keyword in description for keyword in ai_keywords):
        return 'ai-ml'
    
    # Add more categorization logic
    # ...
    
    return 'misc'

def generate_project_markdown(repo):
    """Generate markdown for a project"""
    return f"""
### [{repo['name']}]({repo['html_url']})
**{repo['description'] or 'No description provided'}**

- **Language:** {repo['language'] or 'Not specified'}
- **Stars:** ⭐ {repo['stargazers_count']} | **Forks:** 🍴 {repo['forks_count']}
- **Updated:** {repo['updated_at'][:10]}

---
"""

# Usage
repos = fetch_repositories('ly2xxx')
for repo in repos:
    category = categorize_project(repo)
    markdown = generate_project_markdown(repo)
    # Append to appropriate category file
```

#### 2. Automated Statistics
Create dynamic project statistics:

```python
# scripts/generate_stats.py
def generate_stats_page():
    """Generate project statistics page"""
    total_projects = count_projects()
    languages = get_language_distribution()
    activity = get_recent_activity()
    
    return f"""
# 📊 Project Statistics

## Overview
- **Total Projects:** {total_projects}
- **Total Stars:** {sum_stars()}
- **Languages Used:** {len(languages)}

## Language Distribution
{generate_language_chart(languages)}

## Recent Activity
{generate_activity_timeline(activity)}
"""
```

#### 3. GitHub Actions for Auto-Updates
Enhance the workflow to automatically update content:

```yaml
# .github/workflows/auto-update.yml
name: Auto-Update Catalog

on:
  schedule:
    - cron: '0 0 * * 1'  # Weekly on Monday
  workflow_dispatch:

jobs:
  update:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v4
    
    - name: Setup Python
      uses: actions/setup-python@v4
      with:
        python-version: '3.x'
        
    - name: Update repository data
      run: |
        python scripts/update_catalog.py
        
    - name: Commit changes
      run: |
        git config --local user.email "action@github.com"
        git config --local user.name "GitHub Action"
        git add -A
        git diff --staged --quiet || git commit -m "🤖 Auto-update catalog content"
        git push
```

---

## 🎨 Customization Guide

### Theming and Styling

#### Color Scheme
Update `mkdocs.yml` to change colors:

```yaml
theme:
  name: material
  palette:
    # Light mode
    - scheme: default
      primary: indigo      # Change primary color
      accent: indigo       # Change accent color
      toggle:
        icon: material/brightness-7
        name: Switch to dark mode
    # Dark mode  
    - scheme: slate
      primary: indigo      # Dark mode primary
      accent: indigo       # Dark mode accent
      toggle:
        icon: material/brightness-4
        name: Switch to light mode
```

#### Custom CSS
Add custom styles in `docs/stylesheets/extra.css`:

```css
/* Custom project card styling */
.project-card {
    border: 1px solid var(--md-default-fg-color--lighter);
    border-radius: 8px;
    padding: 1rem;
    margin: 1rem 0;
    background: var(--md-code-bg-color);
}

/* Custom badge styles */
.tech-badge {
    background: var(--md-primary-fg-color);
    color: white;
    padding: 2px 8px;
    border-radius: 12px;
    font-size: 0.8em;
}
```

Then reference in `mkdocs.yml`:
```yaml
extra_css:
  - stylesheets/extra.css
```

#### Navigation Structure
Customize the navigation in `mkdocs.yml`:

```yaml
nav:
  - Home: index.md
  - Projects:
    - Overview: projects/index.md
    - By Technology:
      - Python: projects/python.md
      - JavaScript: projects/javascript.md
      - Go: projects/go.md
    - By Type:
      - Applications: projects/applications.md
      - Libraries: projects/libraries.md
      - Tools: projects/tools.md
  - Blog: blog/index.md      # Add a blog section
  - Resume: resume.md        # Add your resume
  - Contact: contact.md      # Contact information
```

### Advanced Features

#### 1. Search Enhancement
Add custom search configuration:

```yaml
plugins:
  - search:
      lang: en
      separator: '[\s\-,:!=\[\]()"`/]+|\.(?!\d)|&[lg]t;|(?!\b)(?=[A-Z][a-z])'
  - tags:
      tags_file: tags.md
```

#### 2. Blog Integration
Add a blog section using mkdocs-blog-plugin:

```yaml
plugins:
  - blog:
      blog_dir: blog
      blog_toc: true
      post_date_format: medium
      archive_date_format: yyyy
```

#### 3. Social Links and Analytics
```yaml
extra:
  analytics:
    provider: google
    property: G-XXXXXXXXXX
  social:
    - icon: fontawesome/brands/github
      link: https://github.com/ly2xxx
    - icon: fontawesome/brands/linkedin  
      link: https://linkedin.com/in/yourprofile
    - icon: fontawesome/brands/twitter
      link: https://twitter.com/yourhandle
```

#### 4. Project Showcase Templates
Create reusable templates for different project types:

```markdown
<!-- templates/ai-project.md -->
### [{{name}}]({{url}})
**{{description}}**

{{details}}

- **Tech Stack:** {{tech_stack}}
- **Model:** {{model_info}}
- **Dataset:** {{dataset_info}}
- **Performance:** {{metrics}}
- **Status:** {{status}}
- **Stars:** ⭐ {{stars}} | **Forks:** 🍴 {{forks}}

{{#license}}
- **License:** {{license}}
{{/license}}

{{#demo}}
📖 [Live Demo]({{demo}}) | 
{{/demo}}
{{#paper}}
📄 [Paper]({{paper}}) | 
{{/paper}}
🔧 [Documentation]({{url}}#readme)

---
```

---

## 🔧 Technical Architecture

### File Structure
```
catalog/
├── docs/                    # Documentation source
│   ├── index.md            # Homepage
│   ├── about.md            # About page
│   ├── contributing.md     # Contribution guidelines
│   ├── projects/           # Project documentation
│   │   ├── ai-ml.md       # AI/ML projects
│   │   ├── dev-tools.md   # Development tools
│   │   ├── web-apps.md    # Web applications
│   │   ├── learning.md    # Learning resources
│   │   └── poc.md         # Proof of concepts
│   └── stylesheets/       # Custom CSS (optional)
├── scripts/                # Automation scripts (optional)
│   ├── update_catalog.py  # Auto-update script
│   └── generate_stats.py  # Statistics generator
├── .github/
│   └── workflows/
│       └── deploy.yml     # Deployment workflow
├── mkdocs.yml             # MkDocs configuration
├── requirements.txt       # Python dependencies
└── README.md             # This file
```

### Dependencies
- **MkDocs** - Static site generator
- **Material for MkDocs** - Modern theme with advanced features
- **Git Revision Date** - Automatic page timestamps
- **GitHub Actions** - Automated deployment

### Deployment Pipeline
1. **Trigger:** Push to main branch
2. **Build:** Install dependencies and generate static site
3. **Deploy:** Push to gh-pages branch using mkdocs gh-deploy
4. **Live:** Automatically available at ly2xxx.github.io/catalog

---

## 📋 Maintenance Checklist

### Monthly Tasks
- [ ] Review and update project descriptions
- [ ] Add any new repositories to appropriate categories
- [ ] Update star counts and project statuses
- [ ] Check for broken links
- [ ] Review and update technology lists

### Quarterly Tasks  
- [ ] Reorganize categories if needed
- [ ] Update color scheme or theme elements
- [ ] Review and improve navigation structure
- [ ] Add new features or sections
- [ ] Performance audit and optimization

### Annual Tasks
- [ ] Major design refresh consideration
- [ ] Comprehensive content audit
- [ ] Technology stack updates
- [ ] SEO optimization review
- [ ] Analytics review and insights

---

## 🤝 Contributing

### For External Contributors
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Make your changes to the appropriate category files
4. Test locally with `mkdocs serve`
5. Commit your changes (`git commit -m 'Add amazing feature'`)
6. Push to the branch (`git push origin feature/amazing-feature`)
7. Open a Pull Request

### Content Guidelines
- Use clear, concise descriptions
- Include relevant technical details
- Maintain consistent formatting
- Add proper emoji icons for visual appeal
- Ensure all links are functional
- Follow the established project template

### Code Guidelines
- Follow Python PEP 8 for any automation scripts
- Use clear, descriptive variable names
- Add comments for complex logic
- Test all changes locally before submitting

---

## 🆘 Troubleshooting

### Common Issues

#### Deployment Failures
```bash
# Check workflow logs in GitHub Actions
# Common fixes:
git pull origin main
mkdocs build --verbose
```

#### Local Development Issues
```bash
# Clear cache and reinstall
pip cache purge
pip install -r requirements.txt --force-reinstall

# Reset local environment
rm -rf site/
mkdocs serve --clean
```

#### Broken Links
```bash
# Check for broken internal links
mkdocs build --strict

# Validate external links (if you add a link checker)
python scripts/check_links.py
```

#### Search Not Working
- Ensure all markdown files have proper headers
- Rebuild the search index: `mkdocs build --clean`
- Check for special characters in content

### Getting Help
- 📖 [MkDocs Documentation](https://www.mkdocs.org/)
- 🎨 [Material Theme Docs](https://squidfunk.github.io/mkdocs-material/)
- 🚀 [GitHub Actions Docs](https://docs.github.com/en/actions)
- 💬 [Create an Issue](https://github.com/ly2xxx/catalog/issues) for project-specific help

---

## 📈 Future Enhancements

### Short Term (Next 3 months)
- [ ] Automated project metrics collection
- [ ] Interactive project timeline
- [ ] Technology tag filtering
- [ ] Project search by technology stack
- [ ] Mobile app version

### Medium Term (3-6 months)  
- [ ] Integration with GitHub API for real-time data
- [ ] Project dependency visualization
- [ ] Contribution activity heatmap
- [ ] Automated screenshot generation
- [ ] Multi-language support

### Long Term (6+ months)
- [ ] AI-powered project categorization
- [ ] Interactive project recommendation system
- [ ] Portfolio analytics dashboard
- [ ] Integration with other portfolio platforms
- [ ] Video project demonstrations

### Ideas for Expansion
- **Project Metrics Dashboard** - Real-time GitHub statistics
- **Technology Radar** - Visual representation of tech stack evolution
- **Contribution Graph** - Activity visualization across all projects
- **Project Relationships** - Show dependencies and connections
- **Learning Path Generator** - Suggested project study order
- **Community Features** - Comments, ratings, or discussions

---

## 📊 Success Metrics

Track the success of your catalog with these metrics:

### Technical Metrics
- Page load speed (target: <2 seconds)
- Search functionality performance
- Mobile responsiveness score
- SEO optimization rating

### Content Metrics  
- Number of projects documented
- Content freshness (last update dates)
- Link validation passing rate
- Category distribution balance

### Engagement Metrics (if you add analytics)
- Page views and unique visitors
- Time spent on site
- Most popular project categories
- Search query patterns

---

## 📝 License

This catalog project is open source and available under the [MIT License](LICENSE).

Individual projects may have their own licenses - please check each project's repository for specific licensing information.

---

## 🎉 Acknowledgments

- **MkDocs Team** - For the excellent static site generator
- **Material Theme Authors** - For the beautiful, functional theme
- **GitHub** - For hosting and Actions infrastructure  
- **Open Source Community** - For inspiration and best practices

---

*Built with ❤️ using MkDocs and Material Theme. Last updated: September 2025*

**Ready to showcase your projects? Start expanding your catalog today! 🚀**
