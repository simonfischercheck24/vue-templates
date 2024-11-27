<template>
    <div class="text-3xl font-bold underline">
        <h1>{{ title }}</h1>
    </div>
</template>

<script lang="ts">
export default {
    name: 'TheHeader',
    props: {
        title: String,
    },
}
</script>
