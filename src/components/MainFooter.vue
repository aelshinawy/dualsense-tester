<script setup lang="ts">
import GitVersion from './common/GitVersion.vue'
</script>

<template>
  <footer>
    <div class="footer">
      <div class="left">
        <i18n-t keypath="application.footer.copyright" tag="div" scope="global">
          <template #year>
            <span>{{ new Date().getFullYear() }}</span>
          </template>
          <template #author>
            <a href="http://im.daidr.me" target="_blank" class="dou-sc-link">daidr</a>
          </template>
        </i18n-t>
      </div>
      <div class="right">
        <GitVersion />
      </div>
    </div>
  </footer>
</template>

<style scoped lang="scss">
footer {
  @apply select-none;
  @apply w-full px-2;

  .footer {
    @apply max-w-[var(--max-width)] w-full;
    @apply flex justify-between items-center mx-auto my-2;
    @apply dou-sc-container;
  }
}
</style>
