<template>
    <component :is="type" @input="onInput" @focus="onFocus" @blur="onBlur"></component>
</template>

<script setup lang="ts">
const type: "input" | "textarea" = "input";

const emit = defineEmits<{
    (e: "onInput"): void;
    (e: "onFocus"): void;
    (e: "onBlur"): void;
}>();

function onInput(): void {
    console.log("input - dynamic component");
    emit("onInput");
}

function onFocus(): void {
    console.log("focus - dynamic component");
    emit("onFocus");
}

function onBlur(): void {
    console.log("blur - dynamic component");
    emit("onBlur");
}
</script>
