<template>
  <div class="slidev-layout title-content">
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

    <!-- Main content area -->
    <main class="slide-content">
      <slot />
    </main>

    <!-- Footer space (just spacing, no actual content) -->
    <footer class="slide-footer"></footer>
  </div>
</template>

<style scoped>
.slidev-layout.title-content {
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
  /* text-shadow: 0 2px 4px rgba(0, 0, 0, 0.3); */
}

/* Logo positioning (using the existing CSS system) */
.slidev-layout.title-content::before {
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
  overflow-y: scroll;
}

/* Footer space */
.slide-footer {
  position: relative;
  z-index: 5;
  @apply h-4; /* Reduced bottom spacing to give more room to content */
}

/* Typography styles for dark text on light background */
.slide-content :deep(h1) {
  @apply text-3xl font-bold text-gray-900 mb-6;
}

.slide-content :deep(h2) {
  @apply text-2xl font-semibold text-gray-800 mb-4;
}

.slide-content :deep(h3) {
  @apply text-xl font-semibold text-gray-800 mb-3;
}

.slide-content :deep(h4),
.slide-content :deep(h5),
.slide-content :deep(h6) {
  @apply text-lg font-medium text-gray-700 mb-2;
}

.slide-content :deep(p) {
  @apply text-gray-700 mb-4 leading-relaxed;
}

.slide-content :deep(ul),
.slide-content :deep(ol) {
  @apply text-gray-700 mb-4 pl-6;
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

.slide-content :deep(a) {
  @apply text-blue-600 hover:text-blue-800 underline;
}

.slide-content :deep(strong) {
  @apply font-semibold text-gray-900;
}

.slide-content :deep(em) {
  @apply italic;
}

.slide-content :deep(code) {
  @apply bg-gray-100 text-gray-800 px-2 py-1 rounded text-sm font-mono;
}

.slide-content :deep(pre) {
  @apply bg-gray-100 text-gray-800 p-4 rounded-lg mb-4 overflow-x-auto;
  border: 1px solid #e5e7eb;
}

.slide-content :deep(pre code) {
  @apply bg-transparent p-0;
}

.slide-content :deep(blockquote) {
  @apply border-l-4 border-blue-500 pl-4 italic text-gray-600 mb-4;
}

.slide-content :deep(table) {
  @apply w-full border-collapse mb-4;
}

.slide-content :deep(th),
.slide-content :deep(td) {
  @apply border border-gray-300 px-4 py-2 text-left;
}

.slide-content :deep(th) {
  @apply bg-gray-100 font-semibold;
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
  
  .slidev-layout.title-content::before {
    top: 1rem;
    right: 1rem;
    width: 80px;
    height: 36px;
  }
}
</style>
