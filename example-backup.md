---
theme: ./
title: OpenSQZ Theme Demo
---

# OpenSQZ Theme Demo

A custom Slidev theme for OpenSQZ presentations

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer btn" flex="~ justify-center items-center gap-2">
    Press Space for next page <div class="i-carbon:arrow-right inline-block"/>
  </span>
</div>

---
layout: content
---

# Content Page Layout

This is an example of the content page layout, designed for presenting information in a clean, structured format.

<ContentSection title="Key Features" subtitle="What makes this theme special">
- **Professional Design** - Clean, modern look with the OpenSQZ branding
- **Flexible Layouts** - Specialized layouts for different content types
- **Reusable Components** - Built with Vue components for consistency
- **Asset Integration** - Incorporates your logo and background assets
- **Responsive** - Looks great on any screen size
</ContentSection>

<ContentSection title="Code Example" variant="highlight">

```ts
interface Presentation {
  title: string;
  slides: Slide[];
  theme: 'opensqz-theme';
}

function createPresentation(title: string): Presentation {
  return {
    title,
    slides: [],
    theme: 'opensqz-theme'
  };
}
```

</ContentSection>

---
layout: content
---

# Using Components

The theme includes reusable components to maintain consistency across slides.

<ContentSection title="Content Sections" variant="default">
Content sections help organize information with optional titles and subtitles.
They come in three variants: default, highlight, and minimal.

```html
<ContentSection title="Section Title" subtitle="Optional subtitle" variant="default">
  Your content goes here...
</ContentSection>
```
</ContentSection>

<ContentSection title="Typography" variant="minimal">
## Headings
The theme includes styled headings (h1-h6) for clear hierarchy.

### Lists
- Unordered lists
- With consistent styling
- For better readability

1. Ordered lists
2. Also work great
3. With the theme styling
</ContentSection>

---
layout: people
title: Our Team
---

<PersonCard
  name="Jane Smith"
  role="CEO & Founder"
  description="Leading our vision and strategy"
  image="https://images.unsplash.com/photo-1494790108377-be9c29b29330?w=250&h=250&auto=format&fit=crop"
/>

<PersonCard
  name="John Doe"
  role="CTO"
  description="Overseeing our technical direction"
  image="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?w=250&h=250&auto=format&fit=crop"
/>

<PersonCard
  name="Emily Johnson"
  role="Design Lead"
  description="Creating beautiful user experiences"
  image="https://images.unsplash.com/photo-1573497019940-1c28c88b4f3e?w=250&h=250&auto=format&fit=crop"
/>

<PersonCard
  name="Michael Chen"
  role="Lead Developer"
  description="Building robust solutions"
  image="https://images.unsplash.com/photo-1500648767791-00dcc994a43e?w=250&h=250&auto=format&fit=crop"
/>

<PersonCard
  name="Sarah Williams"
  role="Marketing Director"
  description="Growing our market presence"
  image="https://images.unsplash.com/photo-1580489944761-15a19d654956?w=250&h=250&auto=format&fit=crop"
/>

<PersonCard
  name="David Kim"
  role="Product Manager"
  description="Driving product development"
  image="https://images.unsplash.com/photo-1539571696357-5a69c17a67c6?w=250&h=250&auto=format&fit=crop"
/>

---
layout: content
---

# Theme Configuration

The OpenSQZ theme is highly configurable to meet your presentation needs.

<ContentSection title="Layout Options" variant="default">
- **Default** - Standard slide with centered content
- **Cover** - Title slide with prominent branding
- **Content** - Structured layout for detailed information
- **People** - Grid layout for team or personnel slides
</ContentSection>

<ContentSection title="Customization" variant="highlight">
You can customize the theme by modifying the CSS variables in `styles/layout.css`:

```css
:root {
  --slidev-theme-primary: #1e40af;
  --slidev-theme-secondary: #3b82f6;
  --slidev-theme-accent: #60a5fa;
  /* ... other variables */
}
```
</ContentSection>

---
layout: center
class: "text-center"
---

# Thank You!

[Documentation](https://sli.dev) / [GitHub Repo](https://github.com/slidevjs/slidev)
