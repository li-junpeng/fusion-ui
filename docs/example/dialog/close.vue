<script setup lang="ts">
import { ref } from 'vue'
const dialogVisible = ref(false)
</script>

<template>
  <fn-button type="outline" @click=" dialogVisible = true">
    show colse
  </fn-button>
  <fn-dialog
    v-model="dialogVisible"
    title="Tips"
    show-close="false"
  >
    <span>This is a message</span>
    <template #footer>
      <span class="dialog-footer">
        <fn-button type="outline" @click="dialogVisible = false">Cancel</fn-button>
        <fn-button @click="dialogVisible = false">
          Confirm
        </fn-button></span>
    </template>
  </fn-dialog>
</template>

<style scoped>
.dialog-footer button:first-child {
  margin-right: 10px;
}
</style>
