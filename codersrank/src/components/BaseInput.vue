<template>
<div class="input-wrap">
    <label for="">{{ label }}</label>
    <input type="text" :value="modelValue" @input="$emit('update:modelValue')">
</div>
</template>
<script setup lang="ts">
defineProps({
    label: {
        type: String,
        default: "",
    },
    modelValue: {
        type: String,
        default:"",
    }
})
</script>
<style lang="" scoped>
.input-wrap{
    display: flex;
    flex-direction: column;
    input{
        padding: 8px 12px;
        font-size: 16px;
    }
}
</style>