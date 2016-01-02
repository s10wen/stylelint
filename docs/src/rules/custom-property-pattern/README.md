---
layout: page
title: custom-property-pattern
permalink: docs/src/rules/custom-property-pattern/README/
---

# custom-property-pattern

Specify pattern of custom properties.

```css
    a { --foo-bar: 1px; }
/**        ↑
 * The pattern of this */
```

`regex` or `string`

A string will be translated into a RegExp like so `new RegExp(yourString)` — so be sure to escape properly.

### E.g. `/foo-.+/`

The following patterns are considered warnings:

```css
:root { --boo-bar: 0; }
```

The following patterns are *not* considered warnings:

```css
:root { --foo-bar: 0; }
```