<script setup>
import content from "./client-side-security-patches.md?raw";

definePageMeta({
  layout: "policy",
});
</script>

<template>
  <DocsCard :content="content" />
</template>
