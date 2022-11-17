<template>
  <NodeViewWrapper draggable="true" class="tiptap-video">
    <NodeToolbar @delete="deleteNode"></NodeToolbar>
    <iframe width="100%" height="320" :src="`https://www.youtube.com/embed/${node.attrs['data-id']}`" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  </NodeViewWrapper>
</template>

<script setup>
import { NodeViewWrapper, nodeViewProps } from '@tiptap/vue-3'
import NodeToolbar from '../../NodeToolbar.vue'

const props = defineProps(nodeViewProps)

console.log(props)
</script>