<template>
  <div class="flex flex-row justify-center">
    <button class="m-2 p-2 text-2xl text-white bg-tertiary w-32 rounded-md flex flex-row hover:drop-shadow-red-1">
      <ReverseIcon class="text-white"/>
      <p>{{ $t('buttons.reverse') }}</p>
    </button>
  </div>
</template>
  
<script setup>
  import ReverseIcon from '@/components/icons/ReverseIcon.vue'
</script>
  