# 🍄 Mushroom Themes

[![hacs][hacs-badge]][hacs-url]

Mushroom allow you to customize your Mushroom dashboard using [Home Assistant][home-assistant] themes.

![Overview](https://user-images.githubusercontent.com/5878303/152332130-760cf616-5c40-4825-a482-bb8f1f0f5251.png)

## Usage

Just select your theme in your Home Assistant profile settings.

2 themes are available :

-   [Default](docs/themes/default.md)
-   [Square](docs/themes/square.md)

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
git clone https://github.com/piitaya/lovelace-mushroom
```

<!-- Badges -->

[hacs-url]: https://github.com/custom-components/hacs
[hacs-badge]: https://img.shields.io/badge/hacs-custom-orange.svg?style=flat-square

<!-- References -->

[home-assistant]: https://www.home-assistant.io/
[home-assitant-theme-docs]: https://www.home-assistant.io/integrations/frontend/#defining-themes
[hacs]: https://hacs.xyz
