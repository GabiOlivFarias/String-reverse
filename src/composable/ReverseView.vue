<template>
    <div>
        <p class="flex justify-start pl-4 font-regular text-2xl"> 
            {{ $t('subtittle') }}
        </p>
        <PhraseInput />
    </div>
</template>

<script setup>
import PhraseInput from '@/components/globals/input/PhraseInput.vue'
</script>
