<template>
  <NodeViewWrapper draggable="true" class="tiptap-image">
    <NodeToolbar @delete="deleteNode">
      <template #prepend>
        <NodeToolbarItem
          :class="{'bg-green hover:bg-green': parseInt(editor.contentComponent.$parent?.coverId) === parseInt(node.attrs['data-id'])}"
          @click="editor.contentComponent.$emit('cover', node.attrs['data-id'])"
        >
          Обложка
        </NodeToolbarItem>
      </template>
    </NodeToolbar>

    <img :src="node.attrs.src" :data-id="node.attrs['data-id']" :data-src="node.attrs['data-src']" alt="" style="display: block">
  </NodeViewWrapper>
</template>

<script setup>
import { NodeViewWrapper, nodeViewProps } from '@tiptap/vue-3'
import NodeToolbar from '../../NodeToolbar.vue'
import NodeToolbarItem from '../../NodeToolbarItem.vue'

defineProps(nodeViewProps)
</script>