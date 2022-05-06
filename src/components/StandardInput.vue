<template>
    <input @input="onInput" @focus="onFocus" @blur="onBlur" />
</template>

<script setup lang="ts">
const emit = defineEmits<{
    (e: "onInput"): void;
    (e: "onFocus"): void;
    (e: "onBlur"): void;
}>();

function onInput(): void {
    console.log("input - standard input");
    emit("onInput");
}

function onFocus(): void {
    console.log("focus - standard input");
    emit("onFocus");
}

function onBlur(): void {
    console.log("blur - standard input");
    emit("onBlur");
}
</script>
