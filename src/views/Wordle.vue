<template>
  <h1>TEST</h1>
  <WordInput />
  <br style="margin-bottom: 30px" />
  <div style="margin: auto">
    <Keyboard />
  </div>
</template>

<script>
import Keyboard from '@/components/Keyboard.vue'
import WordInput from '@/components/WordInput.vue'

export default {
  name: 'wordle',
  components: { Keyboard, WordInput },
  setup() {},
}
</script>
