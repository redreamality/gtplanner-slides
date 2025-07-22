---
theme: ./
title: Test Slide
---

---
layout: title-content
title: "开源平台发布"
---

# Content Area

This is the content area of the slide with some sample content to test the layout.

## Features

- **Professional Design** - Clean, modern look with OpenSQZ branding
- **Flexible Layouts** - Specialized layouts for different content types
- **Reusable Components** - Built with Vue components for consistency
- **Asset Integration** - Incorporates your logo and background assets
- **Responsive** - Looks great on any screen size

## Code Example

```typescript
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

This layout should match the visual design shown in the reference image with the title in the top-left, logo in the top-right, and content area with proper spacing.

---
layout: intro
title: hi
---

# hi

asdfa

---
layout: section-divider
title: ""
---

## Part Two：This is a section



---
layout: two-column
title: "1"
---

## Part Two：This is a section


::left::
- 1231
- 1231
- 1231

::right::
right 1231
