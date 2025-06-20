<template>
  <ul v-if="nodes && nodes.length > 0">
    <li
        v-for="node in nodes"
        :key="node.id"
    >
      <h3 v-if="node.title">
        {{ node.title }}
      </h3>
      <Branch v-if="node.children && node.children.length > 0"
        :nodes="node.children"
      />
    </li>
  </ul>
</template>
<script setup>
const { nodes } = defineProps({
  nodes: {
    type: Array,
    default: []
  }
});
</script>