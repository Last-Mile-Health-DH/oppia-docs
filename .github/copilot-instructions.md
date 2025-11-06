# Copilot Instructions for OppiaMobile Documentation

## Project Overview
- This repo contains documentation for the OppiaMobile learning platform, primarily built with Sphinx and reStructuredText (`.rst`).
- The platform is designed for low-connectivity settings, focusing on health worker training.
- Courses are authored in Moodle, exported to the OppiaMobile server, and accessed via a mobile app. User activity syncs back to the server when online.

## Key Structure & Files
- Main docs live in `content/`, `overview/`, `technical/`, `implementers/`, and `support/` directories.
- The Sphinx config is in `conf.py`.
- The build system uses the `Makefile` (Linux/macOS) or `make.bat` (Windows).
- Custom styles are in `_static/custom.css`.
- The documentation's entry point is `index.rst`.

## Developer Workflows
- **Build HTML docs:**
  - Linux/macOS: `make html`
  - Windows: `.[4mmake.bat[0m html` (if present)
- **Clean build artifacts:**
  - `make clean` (removes `_build/`)
- **Internationalization:**
  - Uses `sphinx-intl` for translations. See `locale/` for language files.
- **Theme:**
  - Uses `sphinx_rtd_theme` (see `requirements.txt`).

## Conventions & Patterns
- All documentation pages are written in `.rst` format.
- Navigation is managed via `toctree` directives in `index.rst` and section indexes.
- Images and static assets are stored in `images/` and `_static/`.
- Content is organized by topic and audience (e.g., `implementers/`, `technical/`, `content/`).
- Custom CSS can be added to `_static/custom.css` and referenced in `conf.py`.

## Integration Points
- Documentation references the main OppiaMobile server and app, but does not include server/app code here.
- For contributing to the platform itself, see: https://github.com/DigitalCampus/django-oppia

## Examples
- To add a new guide, create a `.rst` file in the appropriate section and update the relevant `index.rst` with a `toctree` entry.
- To add a new language, use `sphinx-intl` to generate `.po` files in `locale/<lang>/LC_MESSAGES/`.

## External Dependencies
- Python packages: `sphinx`, `sphinx_rtd_theme`, `sphinx-intl` (see `requirements.txt`).

---
For questions about platform architecture, see `overview/architecture.rst`.
For technical details, see `technical/` and `conf.py`.
