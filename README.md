# FWERKOR Theme for Nextcloud

A lightweight Nextcloud theme app that makes the standard Nextcloud interface visually consistent with other FWERKOR web properties while preserving Nextcloud's original page structure and behavior.

## What it changes

- FWERKOR light/dark color palette
- typography and spacing feel
- border radii, borders, hover states, and shadows
- primary controls and form focus treatment
- navigation/sidebar/card surfaces
- login/guest page presentation

## What it intentionally does not change

- Nextcloud templates or DOM structure
- routes, controllers, or app behavior
- application-specific layouts
- accessibility semantics
- third-party app JavaScript

The app is intentionally CSS-first. Most of the styling is done by mapping FWERKOR design tokens onto Nextcloud's own CSS custom properties, with a small set of conservative selectors for high-level surfaces.

## Compatibility

- Nextcloud 31–35
- Production baseline: Nextcloud 35.0.1

## Installation

Clone or copy the repository into the Nextcloud custom apps directory as `fwerkor_theme`:

```bash
cd /var/www/html/custom_apps
git clone https://github.com/fwerkor/nextcloud-app-fwerkor-theme.git fwerkor_theme
php /var/www/html/occ app:enable fwerkor_theme
```

No asset build step is required.

## Upgrade strategy

Because this app does not replace Nextcloud templates, upgrades normally only require checking whether any high-level CSS selectors have changed. The primary styling contract is Nextcloud's CSS custom-property layer.

## License

MIT
