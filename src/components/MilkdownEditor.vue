<template>
  <Milkdown />
</template>

<script lang="ts" setup>
import { Crepe } from '@milkdown/crepe'
import { Milkdown, useEditor } from '@milkdown/vue'

useEditor((root) => {
  return new Crepe({ root })
})
</script>
