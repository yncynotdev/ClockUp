<script setup>
import content from "./maintenance-and-refinements.md?raw";

definePageMeta({
  layout: "policy",
});
</script>

<template>
<DocsCard :content="content" />
</template>
