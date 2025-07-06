<!-- src/components/GlitchTextSequence.vue -->
<template>
  <span
    class="glitch"
    :data-text="displayText"
  >{{ displayText }}</span>
</template>

<script setup lang="ts">
import { ref, onMounted, onBeforeUnmount, withDefaults } from 'vue'

/* ---------- props с дефолтами ---------- */
const props = withDefaults(defineProps<{
  /** Список слов/фраз, которые должны появляться по очереди */
  texts: string[]
  /** Длительность «взлома» каждого слова, мс */
  durationMs?: number
  /** Время показа завершённого слова до следующего глитча, мс */
  holdMs?: number
  /** FPS «щелчков» */
  fps?: number
}>(), {
  texts: [],
  durationMs: 1500,
  holdMs: 1000,
  fps: 30
})

/* ---------- реактивное состояние ---------- */
const displayText = ref<string>('')   // то, что видно на экране

/* ---------- вспомогательные вещи ---------- */
const CHARS =
  'ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789!@#$%^&*()_+{}[]<>?/\\|'

const randChar = () => CHARS[Math.floor(Math.random() * CHARS.length)]

/* ---------- основная логика ---------- */
let intervalId: number | undefined
let timeoutId:  number | undefined

function glitchWord(word: string, onDone: () => void) {
  const letters = word.split('')
  if (letters.length === 0) return onDone()

  const step   = 1000 / props.fps
  const frames = Math.ceil(props.durationMs / step)
  let frame = 0

  intervalId = window.setInterval(() => {
    frame++
    const progress = frame / frames
    const reveal   = Math.floor(progress * letters.length)

    displayText.value = letters
      .map((ch, i) => (i < reveal ? ch : randChar()))
      .join('')

    if (frame >= frames) {
      clearInterval(intervalId)
      displayText.value = word                       // гарантируем чистое слово
      timeoutId = window.setTimeout(onDone, props.holdMs)
    }
  }, step)
}

function cycle(index = 0) {
  const nextIndex = (index + 1) % props.texts.length
  glitchWord(props.texts[index], () => cycle(nextIndex))
}

onMounted(() => {
  if (props.texts.length === 0) return        // ничего анимировать
  cycle(0)                                    // запуск цикла
})

onBeforeUnmount(() => {
  clearInterval(intervalId)
  clearTimeout(timeoutId)
})
</script>

<style scoped>
/* те же стили глитча, что и раньше */
.glitch {
  position: relative;
  display: inline-block;
  font-family: 'Courier New', monospace;
  color: #fff;
  animation: flicker 2s infinite linear alternate;
}

@keyframes flicker       { 0%,19%,21%,23%,25%,54%,56%,100%{opacity:.95;} 20%,24%,55%{opacity:.4;} }
@keyframes glitchTop     { 0%,100%{transform:translate(0);} 50%{transform:translate(-2px,-2px);} }
@keyframes glitchBottom  { 0%,100%{transform:translate(0);} 50%{transform:translate( 2px, 2px);} }
</style>
