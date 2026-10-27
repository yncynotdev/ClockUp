<script setup>
import content from "./tooling-modernization.md?raw";

definePageMeta({
  layout: "policy",
});
</script>

<template>
  <DocsCard :content="content" />
</template>
