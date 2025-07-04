# Website Build Structure Explanation

## Overview
This website is built using **Jekyll**, a static site generator that creates fast, secure websites from markdown files and templates. The site uses the **Phantom** theme, which is a minimalist, responsive portfolio theme built with Bootstrap.

## Core Architecture

### 1. **Jekyll Static Site Generator**
- **Technology**: Ruby-based static site generator
- **Purpose**: Converts markdown files and templates into static HTML pages
- **Configuration**: `_config.yml` contains all site settings and build configurations

### 2. **Phantom Theme**
- **Type**: Custom Jekyll theme designed for portfolios
- **Features**: Responsive design, Bootstrap integration, animation effects
- **Customization**: Configured for Ian Yu's personal data science portfolio

## Directory Structure & Build Process

### Core Configuration Files
- **`_config.yml`**: Main Jekyll configuration file containing:
  - Site metadata (title, description, URLs)
  - Build settings (markdown processor, plugins)
  - Pagination settings
  - Theme-specific settings (navigation, contact form, analytics)

- **`Gemfile`**: Ruby dependencies management
  - Specifies Jekyll version and plugins
  - Includes markdown parsing gems (kramdown-parser-gfm, kramdown-syntax-coderay)

- **`phantom.gemspec`**: Theme specification file
  - Defines the theme as a Ruby gem
  - Lists dependencies and theme files

### Layout System (`_layouts/`)
The site uses a hierarchical layout system:

1. **`default.html`**: Base template with header, main content area, and footer
   - Includes MathJax for mathematical expressions
   - Uses Bootstrap grid system

2. **`home.html`**: Homepage layout with post listing and pagination
3. **`inner.html`**: Template for internal pages

### Reusable Components (`_includes/`)
Modular components that can be included in layouts:
- **`header.html`**: Site navigation and branding
- **`footer.html`**: Footer with contact information and links
- **`home-hero.html`**: Homepage hero section
- **`post-content.html`**: Blog post display template
- **`pagination.html`**: Page navigation for blog posts
- **`contact.html`** & **`contact-modal.html`**: Contact form functionality

### Content Management
- **`_posts/`**: Blog posts written in Markdown
  - Files follow naming convention: `YYYY-MM-DD-title.md`
  - Each post has YAML front matter with metadata
  - Current posts cover data science topics (market research, stock forecasting, asset allocation)

- **`about.md`**: About page content in Markdown

### Styling System
- **`_sass/`**: Sass preprocessing for CSS
  - `_bootstrap.scss`: Bootstrap framework integration
  - `_mixins.scss`: Custom CSS mixins
  - `bootstrap/`: Bootstrap component files

- **`css/`**: Compiled CSS files
  - `style.scss`: Main stylesheet that imports Sass files
  - `animate.min.css`: Animation library for visual effects

### Static Assets
- **`img/`**: Image files
- **`js/`**: JavaScript files for interactivity

## Build Process

### 1. **Development Build**
```bash
bundle install          # Install Ruby dependencies
bundle exec jekyll serve # Start development server
```
- Runs on `http://127.0.0.1:4000`
- Auto-regenerates on file changes
- Includes draft posts and future-dated content

### 2. **Production Build**
```bash
bundle exec jekyll build
```
- Generates static files in `_site/` directory
- Optimizes assets and removes development features
- Ready for deployment to any web server

### 3. **Deployment**
- **GitHub Pages**: Configured for automatic deployment
- **Base URL**: `https://ianyu93.github.io/homepage/`
- **Custom Domain**: Can be configured via DNS settings

## Key Features

### 1. **Responsive Design**
- Bootstrap-based responsive grid system
- Mobile-first design approach
- Optimized for all device sizes

### 2. **Blog System**
- Markdown-based content creation
- Automatic pagination (10 posts per page)
- RSS/Atom feed generation (`feed.xml`, `atom.xml`)

### 3. **Contact Integration**
- Modal-based contact form
- Formspree integration for email handling
- Google Analytics tracking

### 4. **Performance Optimization**
- Static site generation for fast loading
- Minified CSS and optimized assets
- CDN integration for external libraries

### 5. **SEO & Analytics**
- Built-in SEO optimization
- Google Analytics integration
- Social media meta tags

## Content Management Workflow

1. **Writing Posts**: Create markdown files in `_posts/` directory
2. **Updating Pages**: Edit markdown files like `about.md`
3. **Styling Changes**: Modify Sass files in `_sass/`
4. **Layout Updates**: Edit HTML templates in `_layouts/` and `_includes/`
5. **Configuration**: Update `_config.yml` for site-wide changes

## Dependencies & External Services

### Ruby Gems
- **Jekyll**: Core static site generator
- **jekyll-paginate**: Pagination functionality
- **kramdown**: Markdown processing
- **bundler**: Dependency management

### External Libraries
- **Bootstrap**: CSS framework for responsive design
- **Animate.css**: CSS animation library
- **MathJax**: Mathematical equation rendering
- **WOW.js**: Animation trigger library

### Services
- **GitHub Pages**: Hosting and deployment
- **Formspree**: Contact form backend
- **Google Analytics**: Website analytics

## Customization Points

This site has been customized for Ian Yu's personal brand:
- **Professional Focus**: Data science and analytics
- **Color Scheme**: Minimalist with professional aesthetics
- **Content Strategy**: Technical blog posts and portfolio showcase
- **Contact Integration**: Professional contact form for client inquiries

The build system allows for easy content updates, theme modifications, and deployment through Git-based workflows.