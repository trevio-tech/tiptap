<template>
  <div class="node-toolbar">
    <div class="node-toolbar-tools">
      <slot name="prepend"></slot>
      <NodeToolbarItem title="Удалить" @click="emit('delete')">
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 461 461">
          <path d="M285 230 456 59c6-6 6-16 0-22L424 5a16 16 0 0 0-22 0L230 176 59 5a16 16 0 0 0-22 0L5 37c-7 6-7 16 0 22l171 171L5 402c-6 6-6 15 0 21l32 33a16 16 0 0 0 22 0l171-171 172 171a16 16 0 0 0 21 0l33-33c6-6 6-15 0-21L285 230z"/>
        </svg>
      </NodeToolbarItem>
    </div>
  </div>
</template>

<script setup>
import NodeToolbarItem from './NodeToolbarItem.vue'
const emit = defineEmits(['delete'])
</script>

<style lang="scss">
.node-toolbar {
  display: flex;
}
.node-toolbar-tools {
  display: flex;
  align-items: center;
  margin-left: auto;
  background-color: rgba(0,0,0,.72);
  border-top-right-radius: 8px;
  border-top-left-radius: 8px;
  overflow: hidden;
}
.node-toolbar-tool {
  display: flex;
  align-items: center;
  color: #fcfcfc;
  min-width: 28px;
  height: 28px;
  padding: 4px;
}
</style>