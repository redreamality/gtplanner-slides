<template>
  <div class="slidev-layout cover">
    <div class="my-auto w-full">
      <slot />
    </div>
  </div>
</template>

<style scoped>
/*
 * COVER LAYOUT
 * This layout is specifically for title slides.
 * It features a dark background with large, centered, light-colored text.
 */
.slidev-layout.cover {
  @apply h-full grid text-center;
  background: url('/assets/background.jpg') center/cover no-repeat;
  color: white; /* Ensure text is readable on the dark background */
}

/* 
 * CRITICAL: DEEP STYLES FOR MARKDOWN CONTENT
 * These rules tell Slidev how to style the raw Markdown from your .md file.
 * Without them, `# Title` would not be rendered as a large heading.
 */
.slidev-layout.cover :deep(h1) {
  @apply text-6xl font-bold leading-tight;
  text-shadow: 0 3px 6px rgba(0, 0, 0, 0.5); /* Add shadow for better readability */
}

.slidev-layout.cover :deep(h2) {
  @apply text-3xl font-light opacity-90 mt-4;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.4);
}

.slidev-layout.cover :deep(p) {
  @apply mt-4 text-lg opacity-80;
}

/* Keep other global styles for consistency, just in case */
.slidev-layout.cover :deep(a) {
  @apply text-blue-300 hover:text-blue-200;
}

.slidev-layout.cover :deep(strong) {
  @apply font-semibold;
}
</style>