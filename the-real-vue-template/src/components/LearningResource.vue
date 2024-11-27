<script setup lang="ts">
import BaseButton from './UI/BaseButton.vue';
import BaseCard from './UI/BaseCard.vue'
</script>

<template>
  <BaseCard>
    <template #header>
      <h5>{{ name }}</h5>
    </template>
    <template #content>
      <BaseButton @click="openLink">{{ link }}</BaseButton>
    </template>
  </BaseCard>
</template>

<script lang="ts">
export default {
  name: 'LearningResource',
  props: {
    id: Number,
    name: String,
    link: String,
  },
  methods: {
    openLink() {
      window.open(this.link)
    },
  },
}
</script>
