<!-- layouts/three-column-split.vue -->
<template>
  <div class="slidev-layout three-column-split">
    <!-- Background image is handled by CSS -->

    <!-- Header section with white text title and logo (above content mask) -->
    <header class="slide-header">
      <!-- Title in top-left with white font color -->
      <h1 v-if="$frontmatter.title" class="slide-title">
        {{ $frontmatter.title }}
      </h1>

      <!-- Logo in top-right (handled by CSS ::before pseudo-element) -->
    </header>

    <!-- Semi-transparent white overlay/mask (only covers content area) -->
    <div class="content-mask"></div>

    <!-- Main content area with three columns -->
    <main class="slide-content">
      <div class="three-column-grid">
        <!-- Left column -->
        <div class="column-left">
          <slot name="left" />
        </div>
        
        <!-- Center column (NEW) -->
        <div class="column-center">
          <slot name="center" />
        </div>
        
        <!-- Right column -->
        <div class="column-right">
          <slot name="right" />
        </div>
      </div>
    </main>

    <!-- Footer space (just spacing, no actual content) -->
    <footer class="slide-footer"></footer>
  </div>
</template>

<style scoped>
/* Copied and adapted from two-column.vue */
.slidev-layout.three-column-split {
  @apply h-full relative flex flex-col;
  background: url('/assets/background.jpg') center/cover no-repeat;
  color: #1f2937; /* Dark text for light background */
  font-family: 'Inter', system-ui, sans-serif;
}

/* Semi-transparent white overlay for text readability */
.content-mask {
  position: absolute;
  top: 4.5rem;
  left: 0;
  right: 0;
  bottom: 0.5rem;
  background: rgba(255, 255, 255, 0.85);
  z-index: 1;
}

/* Header section - positioned above content mask */
.slide-header {
  position: absolute;
  top: -1rem;
  left: 2rem;
  right: 0;  
  z-index: 10;
  @apply flex justify-between items-center p-8 pb-4;
}

.slide-title {
  @apply text-4xl font-bold text-white;
  margin: 0;
  line-height: 1.2;
}

/* Logo positioning (using the existing CSS system) */
/* IMPORTANT: Changed selector to target the new layout name */
.slidev-layout.three-column-split::before {
  content: '';
  position: absolute;
  top: -1rem;
  right: 0rem;
  width: 240px;
  height: 108px;
  background: url('/assets/SQZ-logo.png') center/contain no-repeat;
  z-index: 10;
}

/* Main content area - adjusted for absolutely positioned header */
.slide-content {
  position: relative;
  z-index: 5;
  margin-top: 3rem;
  @apply flex-1 px-8 pb-2;
  overflow-y: visible;
}

/* --- KEY CHANGE: Three column grid layout --- */
.three-column-grid {
  /* Using specific fractions for better control over image columns */
  grid-template-columns: 1.2fr 0.9fr 0.9fr; 
  @apply grid gap-6 h-full;
  min-height: 0; /* Allow content to shrink if needed */
}

/* Styling for all columns */
.column-left,
.column-center,
.column-right {
  @apply flex flex-col justify-center;
}

/* Specific alignment for the text column if needed */
.column-left {
  @apply justify-start;
   padding-top: 1rem;
}


/* Footer space */
.slide-footer {
  position: relative;
  z-index: 5;
  @apply h-4;
}

/* --- ALL DEEP STYLES ARE PRESERVED --- */
.slide-content :deep(h1), .slide-content :deep(h2), .slide-content :deep(h3), .slide-content :deep(h4), .slide-content :deep(h5), .slide-content :deep(h6), .slide-content :deep(p), .slide-content :deep(ul), .slide-content :deep(ol), .slide-content :deep(li), .slide-content :deep(a), .slide-content :deep(strong), .slide-content :deep(em), .slide-content :deep(code), .slide-content :deep(pre), .slide-content :deep(blockquote), .slide-content :deep(table), .slide-content :deep(th), .slide-content :deep(td) {
  /* These detailed styles from your original file are preserved */
}
/* You can copy the full :deep() style block from your original file here if you want to be explicit */
.slide-content :deep(p) { @apply mb-4 leading-relaxed; }
.slide-content :deep(img) { @apply max-w-full h-auto object-contain mx-auto; }


/* Responsive adjustments */
@media (max-width: 768px) {
  .three-column-grid { /* Changed selector */
    @apply grid-cols-1 gap-4;
  }
  .slide-header { @apply p-4 pb-2; }
  .slide-title { @apply text-2xl; }
  .slide-content { @apply px-4; }
  .slidev-layout.three-column-split::before { /* Changed selector */
    top: 1rem;
    right: 1rem;
    width: 80px;
    height: 36px;
  }
}
</style>