<script setup>
import content from "./security-and-stability.md?raw";

definePageMeta({
  layout: "policy",
});
</script>

<template>
  <DocsCard :content="content" />
</template>
