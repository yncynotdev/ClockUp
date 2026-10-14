<script setup>
import content from "./terms-of-service.md?raw";

definePageMeta({
  layout: "policy",
});
</script>

<template>
<DocsCard :content="content" />
</template>
