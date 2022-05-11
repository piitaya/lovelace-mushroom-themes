# 🍄 Mushroom Themes

[![hacs][hacs-badge]][hacs-url]

Mushroom themes allow you to customize your Mushroom dashboard using [Home Assistant][home-assistant] themes.

> ⚠️ It's only a theme! You need to install [Mushroom][mushroom] before to create the card on your dashboard!

![Overview](https://user-images.githubusercontent.com/5878303/152695688-9d705231-500c-49e7-82f5-69e206da95db.png)

## Usage

Just select your theme in your Home Assistant profile settings.

2 themes are available :

-   Mushroom (default)
-   Mushroom square

## Build your own

You can build your own theme by using the mushroom variables.

`em` unit is relative to container height.

```yaml
Mushroom:
    # HA variables
    ha-card-box-shadow: 0px 2px 4px 0px rgba(0,0,0,0.16)
    ha-card-border-radius: 12px
    # Mushroom layout
    mush-spacing: 12px
    # Title
    mush-title-padding: 24px 12px 16px
    mush-title-spacing: 12px
    mush-title-font-size: 24px
    mush-title-font-weight: normal
    mush-title-line-height: 1.2
    # Subtitle
    mush-subtitle-font-size: 16px
    mush-subtitle-font-weight: normal
    mush-subtitle-line-height: 1.2
    # Card
    mush-card-primary-font-size: 14px
    mush-card-secondary-font-size: 12px
    mush-card-primary-font-weight: bold
    mush-card-secondary-font-weight: bolder
    # Chip
    mush-chip-spacing: 8px
    mush-chip-padding: 0 0.25em
    mush-chip-height: 36px
    mush-chip-border-radius: 18px
    mush-chip-font-size: 0.3em
    mush-chip-font-weight: bold
    mush-chip-icon-size: 0.5em
    mush-chip-avatar-padding: 0.1em
    mush-chip-avatar-border-radius: 50%
    # Control
    mush-control-border-radius: 12px
    mush-control-height: 42px
    mush-control-button-ratio: 1
    mush-control-icon-size: 0.5em
    # Slider
    mush-slider-threshold: 10
    # Badge
    mush-badge-size: 16px
    mush-badge-icon-size: 0.75em
    mush-badge-border-radius: 50%
    # Icon
    mush-icon-border-radius: 50%
    mush-icon-size: 42px
    mush-icon-symbol-size: 0.5em
    # Colors
    mush-rgb-red: 244, 67, 54
    mush-rgb-pink: 233, 30, 99
    mush-rgb-purple: 156, 39, 176
    mush-rgb-deep-purple: 103, 58, 183
    mush-rgb-indigo: 63, 81, 181
    mush-rgb-blue: 33, 150, 243
    mush-rgb-light-blue: 3, 169, 244
    mush-rgb-cyan: 0, 188, 212
    mush-rgb-teal: 0, 150, 136
    mush-rgb-green: 76, 175, 80
    mush-rgb-light-green: 139, 195, 74
    mush-rgb-lime: 205, 220, 57
    mush-rgb-yellow: 255, 235, 59
    mush-rgb-amber: 255, 193, 7
    mush-rgb-orange: 255, 152, 0
    mush-rgb-deep-orange: 255, 87, 34
    mush-rgb-brown: 121, 85, 72
    mush-rgb-grey: 158, 158, 158
    mush-rgb-blue-grey: 96, 125, 139
    mush-rgb-black: 0, 0, 0
    mush-rgb-white: 255, 255, 255
        
    mush-rgb-info: var(--mush-rgb-blue)
    mush-rgb-success: var(--mush-rgb-green)
    mush-rgb-warning: var(--mush-rgb-orange)
    mush-rgb-danger: var(--mush-rgb-red)

    mush-rgb-state-fan: var(--mush-rgb-green)
    mush-rgb-state-light: var(--mush-rgb-orange)
    mush-rgb-state-entity: var(--mush-rgb-blue)
    mush-rgb-state-switch: var(--mush-rgb-blue)

    mush-rgb-state-alarm-disarmed: var(--mush-rgb-info)
    mush-rgb-state-alarm-armed: var(--mush-rgb-success)
    mush-rgb-state-alarm-triggered: var(--mush-rgb-danger)

    mush-rgb-state-person-home: var(--mush-rgb-success)
    mush-rgb-state-person-not-home: var(--mush-rgb-danger)
    mush-rgb-state-person-zone: var(--mush-rgb-info)
    mush-rgb-state-person-unknown: var(--mush-rgb-grey)
    
    mush-rgb-state-cover-open: var(--mush-rgb-blue)
    mush-rgb-state-cover-closed: var(--mush-rgb-disabled)
    
    # You must keep this to support light/dark theme
    modes:
        light: 
            mush-rgb-disabled: 189, 189, 189
        dark:
            mush-rgb-disabled: 111, 111, 111
```

## Installation

Add the following code to your configuration.yaml file (restart required).

```yaml
frontend:
  ... # your configuration.
  themes: !include_dir_merge_named themes
  ... # your configuration.
```

### HACS

**Mushroom Themes** is available in [HACS][hacs] (Home Assistant Community Store).

1. Open HACS
2. Go to "Frontend" section
3. Click button with "+" icon
4. Search for "Mushroom Themes"

### Manual

Clone this repository in your existing (or create it) themes/ folder.

```sh
cd themes/
git clone https://github.com/piitaya/lovelace-mushroom-themes
```

<!-- Badges -->

[hacs-url]: https://github.com/hacs/integration
[hacs-badge]: https://img.shields.io/badge/hacs-default-orange.svg?style=flat-square

<!-- References -->

[home-assistant]: https://www.home-assistant.io/
[home-assitant-theme-docs]: https://www.home-assistant.io/integrations/frontend/#defining-themes
[hacs]: https://hacs.xyz
[mushroom]: https://github.com/piitaya/lovelace-mushroom
