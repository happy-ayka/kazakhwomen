---
layout: default
title: Upgrade Summary
---

## Upgrade Summary
- **From:** 0.3.4-beta
- **To:** 0.4.2-beta
- **Date:** 2025-11-11
- **Automated changes:** 60
- **Manual steps:** 12

## Automated Changes Applied

### Configuration (3 files)

- [x] Added Google Sheets integration comments to _config.yml
- [x] Added story_interface configuration section to _config.yml
- [x] Restored WEBrick configuration comment

### Layouts (13 files)

- [x] Updated story layout (multilingual, widgets)
- [x] Updated object layout (multilingual)
- [x] Updated objects index layout (multilingual)
- [x] Updated default layout (multilingual)
- [x] Updated glossary layout (multilingual)
- [x] Updated glossary index layout (multilingual)
- [x] Updated page layout
- [x] Updated index layout (multilingual)
- [x] Updated index layout (site description link styling)
- [x] Updated object layout (coordinate picker buttons)
- [x] Updated story layout (mobile responsive features restored)
- [x] Updated telar styles (mobile responsive features, gallery layout)
- [x] Updated _layouts/index.html: Updated index layout (site description link styling)

### Includes (5 files)

- [x] Updated story-step include (multilingual)
- [x] Updated panels include (widgets support)
- [x] Updated viewer include
- [x] Updated header include (multilingual)
- [x] Updated footer include (multilingual, theme attribution)

### Styles (2 files)

- [x] Updated telar styles (widgets, mobile responsive, site description links)
- [x] Updated assets/css/telar.scss: Updated CSS (mobile navbar, font sizes, title wrapping)

### Scripts (5 files)

- [x] Updated story JavaScript
- [x] Updated telar JavaScript (glossary auto-linking)
- [x] Added widgets JavaScript (carousel, tabs, accordion)
- [x] Updated objects.json endpoint
- [x] Updated story JavaScript (mobile navigation, preloading, transitions)

### Documentation (4 files)

- [x] Updated README
- [x] Updated Google Sheets integration docs
- [x] Updated README (supporter acknowledgments)
- [x] Updated README.md: Updated README (version 0.4.2-beta)

### Other (28 files)

- [x] Created _data/languages directory
- [x] Added English language file (_data/languages/en.yml)
- [x] Added Spanish language file (_data/languages/es.yml)
- [x] Updated IIIF URL warning (multilingual)
- [x] Added accordion widget template
- [x] Added carousel widget template
- [x] Added tabs widget template
- [x] Updated CSV processor (IIIF metadata extraction)
- [x] Updated collection generator (widgets, glossary)
- [x] Updated IIIF tile generator
- [x] Updated Python requirements
- [x] Updated Austin theme (creator attribution)
- [x] Updated Neogranadina theme (creator attribution)
- [x] Updated Paisajes theme (creator attribution)
- [x] Updated Santa Barbara theme (creator attribution)
- [x] Added upgrade notice to index.md
- [x] Restored 'PLEASE DO NOT EDIT BELOW THIS LINE' warning
- [x] Restored '# Collections' header comment
- [x] Restored 'Collections Directory' comment
- [x] Restored '# Build Settings' header comment
- [x] Restored '# Defaults' header comment
- [x] Restored Jekyll dates comment
- [x] Restored 'Telar Settings' comment
- [x] Restored '# Plugins' header comment
- [x] Updated English language file with coordinate picker strings
- [x] Updated Spanish language file with coordinate picker strings
- [x] Updated CHANGELOG
- [x] Updated .github/workflows/build.yml: Updated build workflow (smart IIIF detection with caching)

## Manual Steps Required

Please complete these after merging:

1. Review multilingual configuration in _config.yml (telar_language: "en" or "es") ([guide](https://ampl.clair.ucsb.edu/telar-docs/multilingual-setup))
2. Optionally add widgets to your stories (carousel, tabs, accordion) ([guide](https://ampl.clair.ucsb.edu/telar-docs/widgets))
3. Optionally create glossary terms and add [[term]] links to your content ([guide](https://ampl.clair.ucsb.edu/telar-docs/glossary))
4. Test IIIF metadata auto-population by leaving object fields blank in CSV ([guide](https://ampl.clair.ucsb.edu/telar-docs/iiif-metadata))
5. Add theme creator attribution to your theme YAML file (optional) ([guide](https://ampl.clair.ucsb.edu/telar-docs/themes#creator-attribution))
6. Run "bundle exec jekyll build" to test your upgraded site
7. Update your upgrade workflow file (one-time fix to prevent config comment deletion): (1) Go to https://raw.githubusercontent.com/UCSB-AMPLab/telar/main/.github/workflows/upgrade.yml (2) Select all (Ctrl/Cmd+A) and copy (3) In your repository, navigate to .github/workflows/upgrade.yml (4) Click the pencil icon to edit (5) Select all existing content and delete it (6) Paste the new content (7) Scroll to bottom and click "Commit changes". This fixes a bug that was stripping documentation comments from your _config.yml file during upgrades. ([guide](https://raw.githubusercontent.com/UCSB-AMPLab/telar/main/.github/workflows/upgrade.yml))
8. Run "bundle exec jekyll build" to test your upgraded site
9. Test mobile responsive features on small screens (optional)
10. Try the new coordinate picker buttons in object pages (optional)
11. CRITICAL: The updated build.yml workflow must be merged/committed for IIIF caching to work. If using automated upgrade workflow: Review and MERGE the upgrade pull request - the new build workflow will not take effect until merged. If upgrading locally: COMMIT and PUSH .github/workflows/build.yml - the new workflow is not active until pushed to GitHub. Until the new workflow is active, the IIIF caching protection is not in effect.
12. Test the smart IIIF detection: Make a content-only change (edit a story markdown file), push to GitHub, and verify the build workflow completes faster by skipping IIIF regeneration (optional)

## Resources

- [Full Documentation](https://ampl.clair.ucsb.edu/telar-docs)
- [CHANGELOG](https://github.com/UCSB-AMPLab/telar/blob/main/CHANGELOG.md)
- [Report Issues](https://github.com/UCSB-AMPLab/telar/issues)
