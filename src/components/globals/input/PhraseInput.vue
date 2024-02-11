<template>
    <div class="flex flex-row p-2">
      <input
        id="phrase"
        type="text"
        placeholder="Digite uma frase"
        class="size-12 w-56 cursor-text p-4 m-2 appearance-none border-2 border-solid border-primary"
        @input="onInput">
      <ReverseButton />
    </div>
</template>
  
<script>
import ReverseButton from '@/components/globals/buttons/ReverseButton.vue'

</script>
  