<script setup lang="ts">
import LearningResource from './LearningResource.vue'
</script>

<template>
  <LearningResource
      v-for="resource in resources"
      :key="resource.id"
      :id="resource.id"
      :name="resource.name"
      :link="resource.link"
    />
</template>

<script lang="ts">
export default {
  name: 'StoredResources',
  mounted() {
    console.log('StoredResources component has been mounted!')
  },
  props: {
    resources: Array<{
      id: number
      name: string
      link: string
    }>,
  },
}
</script>
