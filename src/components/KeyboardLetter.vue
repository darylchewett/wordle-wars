<template>
  <button
    class="letterBTN"
    id="{{letter}}"
    v-on:click="$emit('letter-click', letter)"
  >
    {{ letter }}
  </button>
</template>

<script>
export default {
  name: 'KeyboardLetter',
  props: {
    letter: String,
  },
  setup(props) {
    const letter = props.letter
    return {
      letter,
    }
  },
}
</script>
