<template>
  <div class="container flex flex-col gap-3 justify-center items-center py-8">
    <div class="flex flex-col gap-2">
      <label class="text-2xl">{{ text }}</label>
      <InputChild v-model="text"></InputChild> 
    </div>
    <div class="flex flex-col gap-2">
      <p>shadcn</p>
      <Input v-model="text"/>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import { Input } from '@/components/ui/input'
import InputChild from '@/components/input-child/Input-child.vue'; 

let text = ref('Hello World!'); 
</script>
