# Nombredor

[![Greenkeeper badge](https://badges.greenkeeper.io/liitfr/nombredor.svg)](https://greenkeeper.io/)

**φ = (1 + sqrt(5)) / 2**

Basically, an adaptation of [Responsive-Design-with-Golden-Ratio](https://github.com/etchedprints/Responsive-Design-with-Golden-Ratio) that works with **postcss**.

> **Note:** This project is in early development, and versioning is a little different. [Read this](http://markup.im/#q4_cRZ1Q) for more details.

## Code

```sss
:root
  --nombredor: 1.618
  --base-nbdor: 100%
  --nbdor-1: calc(var(--base-nbdor) / var(--nombredor))
  --nbdor-2: calc(var(--base-nbdor) - var(--nbdor-1))
  --nbdor-3: calc(var(--nbdor-2) / var(--nombredor))
  --nbdor-4: calc(var(--nbdor-2) - var(--nbdor-3))
  --nbdor-5: calc(var(--nbdor-4) / var(--nombredor))
  --nbdor-6: calc(var(--nbdor-4) - var(--nbdor-5))
  --nbdor-7: calc(var(--nbdor-6) / var(--nombredor))
  --nbdor-8: calc(var(--nbdor-6) - var(--nbdor-7))
  --nbdor-9: calc(var(--nbdor-8) / var(--nombredor))
  --nbdor-10: calc(var(--nbdor- 8) - var(--nbdor-9))
```

## Some use cases

### Grids

```sss
.full
  width: var(--base-nbdor)
.xl
  width: calc(var(--base-nbdor) - 2 * var(--nbdor-4))
.l
  width: var(--nbdor-1)
.m
  width: var(--nbdor-2)
.s
  width: var(--nbdor-3)
.xs
  width: var(--nbdor-4)
```

### Responsive Padding

```sss
.full,
.xl,
.l,
.m,
.s,
.xs
  padding: var(--nbdor-7)
```

### Color shades

```sss
--base-color: #4f5354
--baseColorLighter: color(var(--base-color) l(var(--nbdor-2)))
--baseColorLight: color(var(--base-color) l(var(--nbdor-4)))
```
