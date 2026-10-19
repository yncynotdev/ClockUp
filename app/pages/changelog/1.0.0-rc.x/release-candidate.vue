<script setup>
import content from "./release-candidate.md?raw";

definePageMeta({
  layout: "policy",
});
</script>

<template>
  <DocsCard :content="content" />
</template>
