<script setup>
import content from "./legacy-integration-complete.md?raw";

definePageMeta({
  layout: "policy",
});
</script>

<template>
<DocsCard :content="content" />
</template>
