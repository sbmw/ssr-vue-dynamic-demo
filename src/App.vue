<template>
    <div>
        <div>
            <label>Dynamic Component</label>
            <DynamicComponent @on-input="onInput" @on-focus="onFocus" @on-blur="onBlur"></DynamicComponent>
        </div>
        <div>
            <label>Standard Input</label>
            <StandardInput @on-input="onInput" @on-focus="onFocus" @on-blur="onBlur"></StandardInput>
        </div>
    </div>
</template>

<script setup lang="ts">
import DynamicComponent from "./components/DynamicComponent.vue";
import StandardInput from "./components/StandardInput.vue";

function onInput(): void {
    console.log("input - app");
}

function onFocus(): void {
    console.log("focus - app");
}

function onBlur(): void {
    console.log("blur - app");
}
</script>

<style>
label {
    display: block;
    font-weight: bold;
}

div > div {
    margin-bottom: 30px;
}
</style>
