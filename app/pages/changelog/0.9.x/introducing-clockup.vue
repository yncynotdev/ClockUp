<script setup>
import content from "./introducing-clockup.md?raw";

definePageMeta({
  layout: "policy",
});
</script>

<template>
  <DocsCard :content="content" />
</template>
