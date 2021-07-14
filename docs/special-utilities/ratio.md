---
title: Ratio
description: Learn about the ratio special utility.
date: 2021-01-08
---

## About Ratio

The `ratio` special utility applies percentage based padding in order to simulate various common screen aspect ratios.

{% include shortcodes/video, id: 'GUQqC8abh6Y' %}

---

## Basic Usage

To apply `ratio`, assign the class `ratio-<aspect-ratio>` to any element.



<div class="radius-md bg-gray-50 p-40 mb-20 gutter-y-40">
  <div>
    <div class="ratio-square relative radius-sm bg-gray-500 color-white">
      <div class="absolute top-50p left-50p transform translate-x-n50p translate-y-n50p font-2xl bold">
        Square 1:1
      </div>
    </div>
  </div>

  <div>
    <div class="ratio-16-9 relative radius-sm bg-gray-500 color-white">
      <div class="absolute top-50p left-50p transform translate-x-n50p translate-y-n50p font-2xl bold">
        16:9
      </div>
    </div>
  </div>

  <div>
    <div class="ratio-4-3 relative radius-sm bg-gray-500 color-white">
      <div class="absolute top-50p left-50p transform translate-x-n50p translate-y-n50p font-2xl bold">
        4:3
      </div>
    </div>
  </div>

  <div>
    <div class="ratio-2-1 relative radius-sm bg-gray-500 color-white">
      <div class="absolute top-50p left-50p transform translate-x-n50p translate-y-n50p font-2xl bold">
        2:1
      </div>
    </div>
  </div>

  <div>
    <div class="ratio-16-10 relative radius-sm bg-gray-500 color-white">
      <div class="absolute top-50p left-50p transform translate-x-n50p translate-y-n50p font-2xl bold">
        16:10
      </div>
    </div>
  </div>
</div>

```html
<div class="gutter-x-20">
  <div>1</div>
  <div>2</div>
  <div>3</div>
  <div>4</div>
</div>
```

```css
.gutter-x-20 > * + * {
  --gutter-right: 0;
  --gutter-left: 1;
  margin: 0 calc(1.25rem * var(--gutter-right)) 0 calc(1.25rem * var(--gutter-left));
}
```

---

## Gutter Reverse

You can reverse direction of the `margin` that is applied by assigning the `gutter-reverse` utility, this can be useful in situations where `flex-row-reverse` or `flex-col-reverse` is applied.

<div class="flex flex-row-reverse radius-md bg-gray-50 p-20 gutter-x-20 gutter-reverse mb-20">
  <div class="flex align-items-center justify-content-center w-40 h-40 radius-sm bg-gray-500 color-white">1</div>
  <div class="flex align-items-center justify-content-center w-40 h-40 radius-sm bg-gray-500 color-white">2</div>
  <div class="flex align-items-center justify-content-center w-40 h-40 radius-sm bg-gray-500 color-white">3</div>
  <div class="flex align-items-center justify-content-center w-40 h-40 radius-sm bg-gray-500 color-white">4</div>
</div>

```html
<div class="flex flex-row-reverse gutter-x-20 gutter-reverse">
  <div>1</div>
  <div>2</div>
  <div>3</div>
  <div>4</div>
</div>
```

---

## Disabling Gutter

To disable this special utility, simply pass in the `gutter` properties to the `excludes` setting in your Uniform configuration.

```scss
@use "uniform" as * with (
  $config: (
    excludes: (
      gutter-x,
      gutter-y,
      gutter-reverse,     
    )
  )
);
```
