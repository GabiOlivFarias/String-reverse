<template>
  <div class="flex flex-row p-2">
    <input
      id="phrase"
      type="text"
      placeholder="Digite uma frase"
      class="size-12 w-56 cursor-text p-4 m-2 appearance-none border-2 border-solid border-primary"
      v-model="inputPhrase"  
    />
    <button @click="reversePhrase" class="m-2 p-2 text-2xl text-white bg-medium-red w-32 rounded-md flex flex-row hover:drop-shadow-red-1">
      Reverter
    </button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputPhrase: ''
    }
  },
  methods: {
    reversePhrase() {
      const phraseArray = this.inputPhrase.split('')
      let reversedPhrase = '';
      for (let i = phraseArray.length - 1; i >= 0; i--) {
        reversedPhrase += phraseArray[i]
      }
      this.inputPhrase = reversedPhrase
    }
  }
}
</script>
