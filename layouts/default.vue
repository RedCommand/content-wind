<template>
  <div class="text-gray-700 dark:text-gray-200">
    <main class="px-4 m-auto lg:px-0 max-w-[864px]">
      <slot />
    </main>
  </div>
</template>

<style lang="postcss">
/* Customize headers to remove default underline */
.prose h2 a,
.prose h3 a {
  @apply no-underline;
  &:hover {
    @apply border-b border-neutral-600 dark:border-neutral-300;
  }
}
</style>
