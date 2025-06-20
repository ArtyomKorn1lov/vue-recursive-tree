<template>
  <Branch
      :nodes="Tree"
  />
</template>
<script setup>
import { Tree } from "@/lib/mocks";
import Branch from "@/components/tree/Branch.vue";
</script>