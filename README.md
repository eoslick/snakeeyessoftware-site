# Snake Eyes Software - Public Site

This repository contains the public-facing website for Snake Eyes Software, built with Hugo and hosted on GitHub Pages.

## Setup

### Prerequisites
- Hugo Extended v0.121.0 or later
- Git

### Installation

#### macOS
```bash
brew install hugo
```

#### Windows
```bash
choco install hugo-extended
```

#### Linux
Download from [Hugo Releases](https://github.com/gohugoio/hugo/releases)

### Local Development

1. Clone this repository:
```bash
git clone https://github.com/YOUR_USERNAME/snakeeyessoftware-site.git
cd snakeeyessoftware-site
```

2. Initialize and update the theme submodule:
```bash
git submodule update --init --recursive
```

3. Run the development server:
```bash
hugo server -D
```

4. Visit http://localhost:1313

## Content Structure

Content is managed in a separate private repository and published here via GitHub Actions.

- `/content/blog/` - Blog posts
- `/content/products/` - Product pages
- `/content/tutorials/` - Tutorial content
- `/static/` - Static assets (images, downloads, etc.)

## Deployment

The site automatically deploys to GitHub Pages when changes are pushed to the `main` branch.

## Theme

This site uses the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme for Hugo.
