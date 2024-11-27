<script setup lang="ts">
import TheHeader from './components/layouts/TheHeader.vue';
import StoredResources from './components/StoredResources.vue';
</script>

<template>
  <header class="w-full p-6 mb-4 bg-slate-400">
    <TheHeader :title="title" />
  </header>
  <main class="flex flex-col justify-between items-center">
    <StoredResources :resources="resources" />
  </main>
</template>

<script lang="ts">
export default {
  name: 'App',
  data: () => ({
    title: 'The real Vue template',
    resources: [
      { id: 1, name: 'Official Guide', link: 'vuejs.org' },
      { id: 2, name: 'Google', link: 'google.com' },
      { id: 3, name: 'MDN', link: 'developer.mozilla.org' },
    ],
  }),
}
</script>
