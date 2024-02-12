<template>
  <div class="md:flex md:flex-row md:p-2">
    <input
      id="phrase"
      type="text"
      :placeholder="$t('placeholders.type_phrase')"
      class="md:size-12 md:w-56 cursor-text p-4 m-2 appearance-none border-2 border-solid border-primary"
      v-model="inputPhrase"/>
    <ReverseButton @click="reversePhrase"/>
  </div>
  <div v-if="reversedPhrase" class="p-2 m-2 result-container font-medium text-2xl">
    <h3>{{ $t('inputs.reverse') }} {{ reversedPhrase }}</h3>
  </div>
</template>

<script>
import ReverseButton from '../buttons/ReverseButton.vue';

export default {
    data() {
        return {
            inputPhrase: '',
            reversedPhrase: ''
        };
    },
    methods: {
        reversePhrase() {
            const phraseArray = this.inputPhrase.split('')
            let reversedPhrase = ''
            for (let i = phraseArray.length - 1; i >= 0; i--) {
                reversedPhrase += phraseArray[i]
            }
            this.reversedPhrase = reversedPhrase
            this.inputPhrase = ''
        }
    },
    components: { ReverseButton }
}
</script>
