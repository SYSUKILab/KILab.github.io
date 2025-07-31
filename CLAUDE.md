# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Hugo static site for the Knowledge Intelligence Lab (KILab) at Sun Yat-sen University. The site uses the Congo theme and is deployed to GitHub Pages at https://kilab.github.io/.

## Architecture

- **Static Site Generator**: Hugo
- **Theme**: Congo (via git submodule from https://github.com/jpanther/congo.git, stable branch)
- **Configuration**: Split configuration in `config/_default/` directory
- **Content**: Markdown files in `content/` directory with multilingual support
- **Theme Customization**: Congo theme provides comprehensive academic website features

## Key Directories

- `/config/_default/`: Hugo configuration files (hugo.toml, params.toml, menus.en.toml, etc.)
- `/content/`: Site content including pages for team, resources, lab activities
- `/themes/congo/`: Git submodule containing the Congo theme
- `/static/`: Static assets (images, etc.)
- `/public/`: Generated site output (ignored in git)

## Development Commands

### Local Development
```bash
hugo server -D --bind 0.0.0.0
```

### Build Site
```bash
hugo
```

### Update Theme
```bash
git submodule update --remote themes/congo
```

## Site Configuration

- **Base URL**: https://kilab.github.io/
- **Default Language**: English
- **Theme**: Congo with "congo" color scheme
- **Layout**: Page layout for homepage with recent posts
- **Features**: Image lazy loading, WebP support, RSS/JSON output

## Content Structure

- Homepage (`content/_index.md`): Lab introduction in Chinese
- Team page (`content/team.md`): Lab members
- Resources section (`content/resources/`): Publications, datasets, conference deadlines
- Lab activities (`content/lab_activities.md`): Laboratory activities
- Posts (`content/posts/`): Blog-style content

## Theme Features

The Congo theme provides:
- Responsive design with light/dark mode
- Academic features (publications, team pages)
- Hugo shortcodes for enhanced content (badges, figures, icons)
- Multi-language support
- SEO optimization

## Deployment

The site is automatically deployed to GitHub Pages via GitHub Actions workflow (`.github/workflows/hugo.yml`).