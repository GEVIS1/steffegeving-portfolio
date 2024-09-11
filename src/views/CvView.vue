<script setup lang="ts">
import pdf from '../assets/Steffen_Geving_CV_English_2024_09_04.pdf'
</script>

<template>
  <main class="pdf-container">
    <!-- <embed class="pdf-preview" :src="pdf" /> -->
    <iframe
      class="pdf-preview"
      src="https://docs.google.com/gview?url=http://cv.geving.dev&embedded=true"
      frameborder="0"
    ></iframe>
    <!-- TODO: Confirm iframe loaded properly -->
  </main>
</template>

<style scoped>
.pdf-container {
  display: flex;
  justify-content: center;
}
.pdf-preview {
  width: 608px;
  height: 90vh;
}
</style>
