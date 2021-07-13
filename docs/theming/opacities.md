---
title: Opacities
description: Learn how to customize and manipulate colors.
date: 2021-01-02
---

## Colors

There are two ways of customizing colors in Uniform; Sass and CSS variables. The native Sass configuration method provides the most flexibility, whereas the CSS variables method is the easiest to configure but comes with limitations.

{% include shortcodes/video, id: 'GUQqC8abh6Y' %}

---

## Customizing via Sass

To customize colors, pass in key value pairs to the `colors` setting in your configuration. Color values must be defined in hexadecimal format. During the build process, colors will be automatically converted to RGB values.

```scss
// main.scss

@use "uniform" as * with (
  $config: (
    colors: (
      primary: #0054CB
    )
  )
)
```

```css
/* main.css */

:root {
  --primary: 0,84,203;
}

.bg-primary {
  --bg-opacity: 1;
  background-color: rgba(var(--primary), var(--bg-opacity));
}
...
```

---

## Disabling Default Colors

If you wish to remove the default colors and add your own, simply pass `null` to any theme property. Additionally, you can add your own by assigning theme settings to the `extend` map.

```scss
// main.scss

@use "uniform" as * with (
  $config: (
    colors: null, // disable default colors

    extend: (
      colors: (
        sunset-50: #FBEBD6,
        sunset-100: #F8D5AF,
        sunset-200: #F1A363,
        sunset-300: #DF742E,
        sunset-400: #CE4700,
        sunset-500: #BE3E00,
        sunset-600: #AD3700,
        sunset-700: #8D2900,
        sunset-800: #792200,
        sunset-900: #661C00,
        sunset-950: #401100,
      )
    )
  )
)
```


---

## Customizing Opacities

Uniform converts each color to RGB values in order to take advantage of special `opacity` utilities that manipulate the alpha channel. You can override and add new opacity levels by passing in key value pairs to the `opacities` setting in your configuration. The following opacity levels are supported by default.

```scss
// main.scss

@use "uniform" as * with (
  $config: (
    opacities: (
      0: 0,
      2: 0.02,
      4: 0.04,
      6: 0.06,
      8: 0.08,
      10: 0.1,
      15: 0.15,
      20: 0.2,
      25: 0.25,
      30: 0.3,
      35: 0.35,
      40: 0.4,
      45: 0.45,
      50: 0.5,
      55: 0.55,
      60: 0.6,
      65: 0.65,
      70: 0.7,
      75: 0.75,
      80: 0.8,
      85: 0.85,
      90: 0.9,
      95: 0.95,
      100: 1,
    )
  )
)
```

---

## Customizing via CDN

If you are using the CDN implementation, you can still customize all existing theme properties by overriding CSS custom properties. This method can be particularly useful for when you just want to get started quickly without worrying about a Sass build process. To see the full list of CSS variables inspect element this page.

```css
/* main.css */

:root {
  --red-hue: 10;
  --red-sat: 63%;
  --blue-hue: 224;
  --blue-sat: 72%;

  --ltn-50: 98%;
  --ltn-600: 64%;
}
```
---

