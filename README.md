# OpenSQZ Slidev Theme

[![NPM version](https://img.shields.io/npm/v/slidev-theme-opensqz-theme?color=3AB9D4&label=)](https://www.npmjs.com/package/slidev-theme-opensqz-theme)

A professional Slidev theme designed for OpenSQZ presentations, featuring custom layouts for content and people pages with integrated branding assets.

## Features

- 🎨 **Professional Design** - Clean, modern look with OpenSQZ branding
- 📱 **Responsive Layouts** - Optimized for different screen sizes
- 🧩 **Reusable Components** - Built with Vue components for consistency
- 🖼️ **Asset Integration** - Incorporates logo and background assets
- 🎯 **Specialized Layouts** - Content and people page layouts
- ⚡ **Performance** - Optimized CSS with backdrop filters and smooth transitions

## Install

Add the following frontmatter to your `slides.md`. Start Slidev then it will prompt you to install the theme automatically.

<pre><code>---
theme: <b>opensqz-theme</b>
---</code></pre>

Learn more about [how to use a theme](https://sli.dev/guide/theme-addon#use-theme).

## Layouts

This theme provides the following layouts:

### `default`
The standard layout with OpenSQZ branding and background.

### `cover`
Title slide layout with prominent branding and centered content.

```yaml
---
layout: cover
---

# Your Presentation Title
Subtitle or description
```

### `content`
Structured layout for detailed information with header, body, and footer sections.

```yaml
---
layout: content
---

# Page Title

<ContentSection title="Section Title" subtitle="Optional subtitle">
Your content here...
</ContentSection>
```

### `people`
Grid layout specifically designed for displaying team members or personnel.

```yaml
---
layout: people
title: Our Team
---

<PersonCard
  name="John Doe"
  role="CEO"
  description="Leading our vision"
  image="/path/to/image.jpg"
/>
```

### `section-divider`
Clean section divider layout for marking transitions between presentation sections. Features centered content without content mask overlay.

```yaml
---
layout: section-divider
title: "Section Title"
---

# New Section

This marks the beginning of a new section in your presentation.
```

## Components

This theme provides the following components:

### `<PersonCard>`
Display individual team members with image, name, role, and description.

**Props:**
- `name` (required): Person's name
- `role`: Job title or role
- `description`: Brief description
- `image`: Profile image URL (optional, shows initials if not provided)

### `<ContentSection>`
Organize content with optional titles and styling variants.

**Props:**
- `title`: Section title
- `subtitle`: Optional subtitle
- `variant`: Styling variant (`default`, `highlight`, `minimal`)

### `<LogoHeader>`
Display the OpenSQZ logo with optional title content.

**Props:**
- `title`: Header title
- `subtitle`: Header subtitle
- `showTitle`: Whether to show title content alongside logo

## Customization

### Colors
Customize the theme colors by modifying CSS variables in your slides:

```css
<style>
:root {
  --slidev-theme-primary: #1e40af;
  --slidev-theme-secondary: #3b82f6;
  --slidev-theme-accent: #60a5fa;
  --slidev-theme-background: #0f172a;
  --slidev-theme-surface: rgba(30, 64, 175, 0.1);
  --slidev-theme-text: #f8fafc;
  --slidev-theme-text-muted: #cbd5e1;
  --slidev-theme-border: rgba(59, 130, 246, 0.2);
}
</style>
```

### Assets
Replace the default assets in the `assets/` directory:
- `SQZ-logo.png` - Company logo (recommended size: 120px width)
- `background.jpg` - Background image (recommended: high resolution gradient or pattern)

## Contributing

- `pnpm install`
- `pnpm dev` to start theme preview of `example.md`
- Edit the `example.md` and style to see the changes
- `pnpm export` to generate the preview PDF
- `pnpm screenshot` to generate the preview PNG
