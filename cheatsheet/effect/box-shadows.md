---
title: Box Shadows
description: Visual reference of all default box-shadows.
date: 2021-01-03
---

## Drop Shadow Effects

The following table visually represents all drop shadow effects that are available.

<div class="bg-gray-100 p-20 radius-lg">
  <div class="grid grid-cols-1 gap-20">
    <div class="h-40 shadow-2xs bg-white radius-sm"></div>
    <div class="h-40 shadow-xs bg-white radius-sm"></div>
    <div class="h-40 shadow-sm bg-white radius-sm"></div>
    <div class="h-40 shadow-md bg-white radius-sm"></div>
    <div class="h-40 shadow-lg bg-white radius-sm"></div>
    <div class="h-40 shadow-xl bg-white radius-sm"></div>
    <div class="h-40 shadow-2xl bg-white radius-sm"></div>
  </div>
</div>

---

## Semantic Effects

The following table visually represents all input states and other semantic effects that are available.

<div class="bg-gray-100 p-20 radius-lg">
  <div class="grid grid-cols-1 gap-20">
    <input type="text" class="h-40 shadow-focus bg-white radius-sm" placeholder="Focus">
    <input type="text" class="h-40 shadow-success bg-white radius-sm" placeholder="Success">
    <input type="text" class="h-40 shadow-warning bg-white radius-sm" placeholder="Warning">
    <input type="text" class="h-40 shadow-danger bg-white radius-sm" placeholder="Danger">
    <input type="text" class="h-40 shadow-info bg-white radius-sm" placeholder="Info">
  </div>
</div>

---

## Class List

Use the following table for `box-shadow` class reference.

| Class | Value |
| - | - |
| `shadow-2xs` | `0 1px 2px rgba(var(--gray-500), 0.1)` {.align-top } |
| `shadow-xs` | `0 2px 4px rgba(var(--gray-500), 0.15)` {.align-top } |
| `shadow-sm` | `0 3px 6px rgba(var(--gray-500), 0.2)` {.align-top } |
| `shadow-md` | `0 4px 8px rgba(var(--gray-500), 0.25)` {.align-top } |
| `shadow-lg` | `0 6px 12px rgba(var(--gray-500), 0.3)` {.align-top } |
| `shadow-xl` | `0 12px 24px rgba(var(--gray-500), 0.35)` {.align-top } |
| `shadow-2xl` | `0 24px 48px rgba(var(--gray-500), 0.4)` {.align-top } |
| `shadow-focus` | `0 0 0 4px rgba(var(--blue-500), 0.2)` {.align-top } |
| `shadow-success` | `0 0 0 4px rgba(var(--green-500), 0.2)` {.align-top } |
| `shadow-warning` | `0 0 0 4px rgba(var(--yellow-500), 0.2)` {.align-top } |
| `shadow-danger` | `0 0 0 4px rgba(var(--red-500), 0.2)` {.align-top } |
| `shadow-info` | `0 0 0 4px rgba(var(--teal-500), 0.2)` {.align-top } |

{ .text-left style="--markdown-table-cell-padding: 0.75em;" }

---

## Basic Usage

Apply box shadow effect with the `shadow-<size>` utility.

```html
<div class="shadow-lg ...">
  ...
</div>
```

---

## CSS Variables

Customize radiuses by overriding the following CSS custom properties.

```css
:root {
  --shadow-2xs: 0 1px 2px rgba(var(--gray-500), 0.1);
  --shadow-xs: 0 2px 4px rgba(var(--gray-500), 0.15);
  --shadow-sm: 0 3px 6px rgba(var(--gray-500), 0.2);
  --shadow-md: 0 4px 8px rgba(var(--gray-500), 0.25);
  --shadow-lg: 0 6px 12px rgba(var(--gray-500), 0.3);
  --shadow-xl: 0 12px 24px rgba(var(--gray-500), 0.35);
  --shadow-2xl: 0 24px 48px rgba(var(--gray-500), 0.4);

  --shadow-focus: 0 0 0 4px rgba(var(--blue-500), 0.2);
  --shadow-success: 0 0 0 4px rgba(var(--green-500), 0.2);
  --shadow-warning: 0 0 0 4px rgba(var(--yellow-500), 0.2);
  --shadow-danger: 0 0 0 4px rgba(var(--teal-500), 0.2);
}
```

