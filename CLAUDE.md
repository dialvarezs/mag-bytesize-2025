# Slidev Project Memory

## Slidev Core Syntax

### Slide Structure
- Slides are separated by `---` with blank lines
- Entry point: `./slides.md`
- Each slide can have optional YAML frontmatter for configuration
- First frontmatter block = headmatter (configures entire presentation)
- Subsequent frontmatter blocks = individual slide config

### Two-Column Layouts

**Built-in `two-cols` layout:**
```yaml
---
layout: two-cols
layoutClass: gap-16  # Optional: adds spacing
---

Left column content

::right::

Right column content
```

**Built-in `two-cols-header` layout:**
```yaml
---
layout: two-cols-header
---

Header spanning both columns

::left::

Left content

::right::

Right content
```

### Other Useful Layouts
- `image-left` / `image-right` - Image on one side, content on other
- `iframe-left` / `iframe-right` - Embed web pages
- `center`, `cover`, `default`, `intro`, `quote`, `section`, etc.

### Styling with UnoCSS
Slidev includes UnoCSS (Tailwind-like utilities):

```markdown
<div class="grid grid-cols-2 gap-4">
  <div>First column</div>
  <div>Second column</div>
</div>

<div class="flex items-center justify-center h-full">
  Centered content
</div>

<div class="absolute left-30px bottom-30px">
  Positioned element
</div>
```

### Components
- `<Transform>` - Scale/transform elements
- `<Arrow>` - Draw arrows between elements
- `<Toc>` - Table of contents
- `<v-drag>` - Make elements draggable
- `<v-click>` - Control animations/visibility

### Code & Diagrams
- Syntax highlighting with Shiki
- LaTeX math with KaTeX (`$inline$` or `$$block$$`)
- Mermaid diagrams (flowcharts, sequence, mindmap)
- PlantUML diagrams

## Light-Icons Theme

### Installation
```yaml
---
theme: light-icons
---
```

### Available Layouts

#### 1. Intro
Basic introduction slide with background image:
```yaml
---
layout: intro
image: 'https://source.unsplash.com/collection/94734566/1920x1080'
---
```

#### 2. Image Header Intro (
**Best for title slides** - logo at top, content below:
```yaml
---
layout: image-header-intro
imageHeader: './images/logo.png'
imageRight: './images/side-graphic.png'  # Optional
---

# Your Title

**Subtitle or affiliation**

Date
```

#### 3. Dynamic Image
Flexible layout with configurable positioning:
```yaml
---
layout: dynamic-image
image: './path/to/image.png'
equal: true      # Equal width columns (true/false)
left: false      # Image position (true=left, false=right)
upperImage: ''   # Optional second image
---

Your content here
```

**Variations:**
- `equal: true, left: false` - Equal columns, image right
- `equal: false, left: false` - Unequal columns, image right (larger)
- `equal: false, left: true` - Unequal columns, image left (larger)
- With `upperImage` - Dual images for split layouts

#### 4. Center Image
```yaml
---
layout: center-image
image: './images/centered.png'
---
```

#### 5. Left Image
```yaml
---
layout: left-image
image: './images/left-side.png'
equal: true
---
```

### Components
- `<LightIcon>` - Light-weighted icon elements
- `<IconBox>` - Styled wrapper for elegant icon presentation

### Features
- 100% light & dark mode compatible
- All layouts adapt automatically to theme
- Responsive design
- Integration with light-icons library

## Project-Specific Notes

### Current Setup
- Theme: `light-icons`
- Main file: `slides.md`
- Logo location: `./images/mag_logo_mascot_light.png`
- Transition: `slide-left`
- MDC syntax: enabled

### Title Slide
Using `image-header-intro` layout for professional title slide with logo at top and credentials below.

## Best Practices

1. **Prefer built-in layouts** over custom HTML/CSS when possible
2. **Use theme-specific layouts** (like `image-header-intro`) for better consistency
3. **Use `::right::`** delimiter for two-column layouts (not HTML divs)
4. **Use UnoCSS utilities** for styling (Tailwind-like classes)
5. **Use frontmatter parameters** instead of manual positioning
6. **Keep layouts simple** - let the theme handle the design

## Common Patterns

### Centered content in columns
```markdown
<div class="flex flex-col justify-center h-full">
  Content vertically centered
</div>
```

### Custom CSS Grid
```markdown
<div class="grid grid-cols-[40%_60%] gap-8">
  <div>40% column</div>
  <div>60% column</div>
</div>
```

### Presenter Notes
```markdown
---
layout: cover
---

# Slide Content

<!-- This is a **note** for presenter mode -->
```

## Resources
- [Slidev Docs](https://sli.dev)
- [Light-Icons Theme](https://github.com/lightvue/slidev-theme-light-icons)
- [UnoCSS Docs](https://unocss.dev)
