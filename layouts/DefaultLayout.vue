<template>
  <div class="min-h-screen flex flex-col bg-zinc-800">
    <SiteHeader />

    <div class="flex-grow">
      <slot />
    </div>

    <SiteFooter />
  </div>
</template>

<script setup></script>
