<template>
  <div class="keyboardWordle">
    <table>
      <tr>
        <td v-for="letter in keyboardLine1">
          <KeyboardLetter
            :letter="letter"
            v-on:letter-click="handleLetterClick(letter)"
          />
        </td>
      </tr>
      <tr style="margin: auto">
        <td v-for="letter in keyboardLine2">
          <KeyboardLetter
            :letter="letter"
            v-on:letter-click="handleLetterClick(letter)"
          />
        </td>
      </tr>
      <tr>
        <td v-for="letter in keyboardLine3">
          <KeyboardLetter
            :letter="letter"
            v-on:letter-click="handleLetterClick(letter)"
          />
        </td>
      </tr>
    </table>
  </div>
</template>

<script>
import KeyboardLetter from '@/components/KeyboardLetter.vue'

export default {
  name: 'Keyboard',
  components: {
    KeyboardLetter,
  },
  setup() {
    const keyboardLine1 = ['Q', 'W', 'E', 'R', 'T', 'Y', 'U', 'I', 'O', 'P']
    const keyboardLine2 = ['A', 'S', 'D', 'F', 'G', 'H', 'J', 'K', 'L']
    const keyboardLine3 = ['Z', 'X', 'C', 'V', 'B', 'N', 'M']

    function handleLetterClick(letter) {
      console.log(letter)
    }

    return {
      keyboardLine1,
      keyboardLine2,
      keyboardLine3,
      handleLetterClick,
    }
  },
}
</script>

<style>
.keyboardWordle {
  margin: auto;
  width: 60vw;
}
td {
  border: 1px, solid, black;
}
.letterBTN {
  width: 40px;
  font-size: large;
}
</style>
