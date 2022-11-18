<template>
  <button class="node-toolbar-tool" type="button" :title="title" @click="$emit('click')">
    <slot></slot>
  </button>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
    }
  }
}
</script>