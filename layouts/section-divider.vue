<template>
  <div class="slidev-layout section-divider">
    <!-- Background image is handled by CSS -->

    <!-- Header section with white text title and logo (above section mask) -->
    <header class="slide-header">
      <!-- Title in top-left with white font color -->
      <h1 v-if="$frontmatter.title" class="slide-title">
        {{ $frontmatter.title }}
      </h1>

      <!-- Logo in top-right (handled by CSS ::before pseudo-element) -->
    </header>

    <!-- Horizontal section mask for section divider -->
    <div class="section-mask"></div>

    <!-- Main content area - centered for section divider -->
    <main class="slide-content">
      <div class="section-content">
        <slot />
      </div>
    </main>

    <!-- Footer space (just spacing, no actual content) -->
    <footer class="slide-footer"></footer>
  </div>
</template>

<style scoped>
.slidev-layout.section-divider {
  @apply h-full relative flex flex-col;
  background: url('/assets/background.jpg') center/cover no-repeat;
  color: #1f2937; /* Dark text for light background with section mask */
  font-family: 'Inter', system-ui, sans-serif;
}

/* Horizontal section mask for section divider - smaller height */
.section-mask {
  position: absolute;
  top: 45%;
  left: 0%;
  right: 0%;
  transform: translateY(-50%);
  height: 30%;
  background: rgba(255, 255, 255, 0.85);
  z-index: 1;
  border-radius: 8px;
}

/* Header section - positioned above section mask */
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
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.3);
}

/* Logo positioning (using the existing CSS system) */
.slidev-layout.section-divider::before {
  content: '';
  position: absolute;
  top: -1rem;
  right: 0rem;
  width: 240px;
  height: 108px;
  background: url('/assets/SQZ-logo.png') center/contain no-repeat;
  z-index: 10;
}

/* Main content area - centered for section divider effect */
.slide-content {
  position: relative;
  z-index: 5;
  @apply flex-1 flex items-center justify-center px-8;
}

.section-content {
  @apply text-center max-w-4xl;
}

/* Footer space */
.slide-footer {
  position: relative;
  z-index: 5;
  @apply h-4;
}

/* Typography styles for dark text on light background (with section mask) */
.slide-content :deep(h1) {
  @apply text-5xl font-bold text-gray-900 mb-8;
}

.slide-content :deep(h2) {
  @apply text-4xl font-semibold text-gray-800 mb-6;
}

.slide-content :deep(h3) {
  @apply text-3xl font-semibold text-gray-800 mb-4;
}

.slide-content :deep(h4),
.slide-content :deep(h5),
.slide-content :deep(h6) {
  @apply text-2xl font-medium text-gray-700 mb-3;
}

.slide-content :deep(p) {
  @apply text-gray-700 mb-4 leading-relaxed text-lg;
}

.slide-content :deep(ul),
.slide-content :deep(ol) {
  @apply text-gray-700 mb-4 pl-6 text-lg;
}

.slide-content :deep(li) {
  @apply mb-2;
}

.slide-content :deep(ul li) {
  @apply list-disc;
}

.slide-content :deep(ol li) {
  @apply list-decimal;
}

.slide-content :deep(strong) {
  @apply font-bold text-gray-900;
}

.slide-content :deep(em) {
  @apply italic text-gray-600;
}

.slide-content :deep(code) {
  @apply bg-gray-100 text-gray-800 px-2 py-1 rounded text-sm font-mono;
}

.slide-content :deep(pre) {
  @apply bg-gray-100 text-gray-800 p-4 rounded-lg mb-4 overflow-x-auto;
  border: 1px solid #e5e7eb;
}

.slide-content :deep(blockquote) {
  @apply border-l-4 border-blue-500 pl-4 italic text-gray-600 mb-4;
}

.slide-content :deep(a) {
  @apply text-blue-600 hover:text-blue-800 underline;
}

/* Responsive adjustments */
@media (max-width: 768px) {
  .slide-header {
    @apply p-4 pb-2;
  }
  
  .slide-title {
    @apply text-2xl;
  }
  
  .slide-content {
    @apply px-4;
  }
  
  .section-content {
    @apply max-w-full;
  }
  
  .slide-content :deep(h1) {
    @apply text-3xl mb-6;
  }

  .slide-content :deep(h2) {
    @apply text-2xl mb-4;
  }

  .slide-content :deep(p),
  .slide-content :deep(ul),
  .slide-content :deep(ol) {
    @apply text-base;
  }
  
  .slidev-layout.section-divider::before {
    top: 1rem;
    right: 1rem;
    width: 80px;
    height: 36px;
  }
}
</style>
