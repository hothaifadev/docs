<script setup lang="ts">
import { ref, watch } from 'vue'

const showWhyVue = ref(false)

watch(
  () => showWhyVue,
  (value) => {
    value
      ? (document.documentElement.style.overflow = 'hidden')
      : (document.documentElement.style.overflow = 'auto')
  }
)
</script>

<template>
</template>

<style scoped>
#vuemastery-action {
  font-size: 16px;
  display: inline-block;
  border-radius: 8px;
  transition: background-color 0.5s, color 0.5s;
  position: relative;
  font-weight: 600;
  background-color: var(--vt-c-green);
  color: #fff;
  margin-right: 18px;
  padding: 8px 1em 8px 3em;
}

.dark #vuemastery-action {
  color: var(--vt-c-indigo);
}

#vuemastery-action:hover {
  background-color: var(--vt-c-green-dark);
  transition-duration: 0.2s;
}

.dark #vuemastery-action:hover {
  background-color: var(--vt-c-green-light);
}

.icon-play {
  display: inline;
  position: absolute;
  left: 15px;
  top: 8px;
  margin-left: 2px;
  fill: currentColor;
  width: 1.5em;
}

.vuemastery-modal-mask {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background: rgba(0, 0, 0, 0.2);
  z-index: 30;
  transition: opacity 0.3s ease;
}

.vuemastery-modal-wrapper {
  display: block;
  box-sizing: border-box;
  border-radius: 8px;
  position: fixed;
  width: 75%;
  height: auto;
  padding: 0.5em;
  background-color: #f9f9f9;
  box-shadow: 0 0 10px rgb(0 0 0 / 20%);
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 40;
}

.dark .vuemastery-modal-wrapper {
  background-color: var(--vt-c-bg-soft);
}

.vuemastery-modal-content {
  margin-bottom: 10px;
}

.vuemastery-video-space {
  position: relative;
  padding: 56.25% 0 0 0;
}

.vuemastery-modal-footer-text {
  color: var(--vt-c-text-2);
  margin-bottom: 0.5em;
  text-align: center;
  word-spacing: 0.05em;
  font-size: 12px;
}

.vuemastery-modal-footer-text a {
  color: #42b983;
  font-weight: 600;
}

.dark .vuemastery-modal-footer-text {
  color: var(--vt-c-text-2);
  font-weight: 600;
}

@media (max-width: 576px) {
  #vuemastery-action {
    display: block;
    margin: 0px auto;
    width: 150px;
  }
}
</style>
