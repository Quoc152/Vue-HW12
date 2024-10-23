<template>
    <div>
        <input 
            class="border border-black rounded-sm" 
            type="text" 
            :value="modelValue" 
            @input="onInput" 
        />
    </div>
</template>

<script setup>
const props = defineProps({
    modelValue: {
        type: String,
        required: true,
    },
});

const emit = defineEmits(['update:modelValue']);

// Hàm xử lý sự kiện input
const onInput = (event) => {
    emit('update:modelValue', event.target.value); 
};
</script>
