<template>
  <div class="slidev-layout title-content">
    <!-- Header with title and logo, positioned above the content mask -->
    <header class="slide-header">
      <h1 v-if="$frontmatter.title" class="slide-title">
        {{ $frontmatter.title }}
      </h1>
    </header>
    
    <!-- Semi-transparent overlay for content readability -->
    <div class="content-mask"></div>

    <!-- Main content area -->
    <main class="slide-content">
      <div class="content-wrapper">
        <slot />
      </div>
    </main>

    <!-- Footer spacing -->
    <footer class="slide-footer"></footer>
  </div>
</template>

<style scoped>
/* -------------------------------------------------- */
/* 1. THEME VARIABLES & BASE LAYOUT
/* -------------------------------------------------- */
.slidev-layout.title-content {
  /* Shared CSS Variables for consistency */
  --header-y-offset: -1rem;
  --header-height: 4.5rem;
  --footer-height: 0.5rem;
  --content-padding-x: 2rem;

  --mask-background: rgba(255, 255, 255, 0.85);
  --title-color: #ffffff;
  --text-color-main: #1f2937;

  --z-index-mask: 1;
  --z-index-content: 5;
  --z-index-header: 10;
  
  /* Base styles */
  @apply h-full relative flex flex-col;
  background: url('/assets/background.jpg') center/cover no-repeat;
  color: var(--text-color-main);
  font-family: 'Inter', system-ui, sans-serif;
}

.slidev-layout.title-content::before {
  content: '';
  position: absolute;
  top: var(--header-y-offset);
  right: 0rem;
  width: 240px;
  height: 108px;
  background: url('/assets/SQZ-logo.png') center/contain no-repeat;
  z-index: var(--z-index-header);
}

/* -------------------------------------------------- */
/* 2. LAYOUT STRUCTURE
/* -------------------------------------------------- */
.slide-header {
  position: absolute;
  top: var(--header-y-offset);
  left: var(--content-padding-x);
  right: var(--content-padding-x);
  z-index: var(--z-index-header);
  @apply flex justify-between items-center pt-8 pb-4;
}

.slide-title {
  @apply text-4xl font-bold;
  color: var(--title-color);
  margin: 0;
  line-height: 1.2;
}

.content-mask {
  position: absolute;
  top: var(--header-height);
  bottom: var(--footer-height);
  left: 0;
  right: 0;
  background: var(--mask-background);
  z-index: var(--z-index-mask);
}

.slide-content {
  position: relative;
  z-index: var(--z-index-content);
  margin-top: calc(var(--header-height) - 1rem); /* Give some space */
  padding-left: var(--content-padding-x);
  padding-right: var(--content-padding-x);
  @apply flex-1 pb-2;
  overflow-y: visible;
}

.slide-footer {
  position: relative;
  height: var(--footer-height);
  z-index: var(--z-index-content);
}

/* -------------------------------------------------- */
/* 3. MAIN CONTENT WRAPPER
/* -------------------------------------------------- */
.content-wrapper {
  @apply h-full flex flex-col justify-center;
}


/* -------------------------------------------------- */
/* 4. GLOBAL TYPOGRAPHY & ELEMENT STYLES (RESTORED)
/* -------------------------------------------------- */
.slide-content :deep(h1) { @apply text-3xl font-bold text-gray-900 mb-6; }
.slide-content :deep(h2) { @apply text-2xl font-semibold text-gray-800 mb-4; }
.slide-content :deep(h3) { @apply text-xl font-semibold text-gray-800 mb-3; }
.slide-content :deep(h4),
.slide-content :deep(h5),
.slide-content :deep(h6) { @apply text-lg font-medium text-gray-700 mb-2; }
.slide-content :deep(p) { @apply text-gray-700 mb-4 leading-relaxed; }
.slide-content :deep(ul),
.slide-content :deep(ol) { @apply text-gray-700 mb-4 pl-6; }
.slide-content :deep(li) { @apply mb-2; }
.slide-content :deep(ul li) { @apply list-disc; }
.slide-content :deep(ol li) { @apply list-decimal; }
.slide-content :deep(a) { @apply text-blue-600 hover:text-blue-800 underline; }
.slide-content :deep(strong) { @apply font-semibold text-gray-900; }
.slide-content :deep(em) { @apply italic; }
.slide-content :deep(code) { @apply bg-gray-100 text-gray-800 px-2 py-1 rounded text-sm font-mono; }
.slide-content :deep(pre) { @apply bg-gray-100 text-gray-800 p-4 rounded-lg mb-4 overflow-x-auto; border: 1px solid #e5e7eb; }
.slide-content :deep(pre code) { @apply bg-transparent p-0; }
.slide-content :deep(blockquote) { @apply border-l-4 border-blue-500 pl-4 italic text-gray-600 mb-4; }
.slide-content :deep(table) { @apply w-full border-collapse mb-4; }
.slide-content :deep(th),
.slide-content :deep(td) { @apply border border-gray-300 px-4 py-2 text-left; }
.slide-content :deep(th) { @apply bg-gray-100 font-semibold; }

/* -------------------------------------------------- */
/* 5. RESPONSIVE ADJUSTMENTS
/* -------------------------------------------------- */
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