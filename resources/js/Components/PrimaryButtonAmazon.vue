<template>
    <button class="a-button-text a-button a-button-span12 a-button-primary">
          <slot />
    </button>
</template>
<style>
.a-button-primary {
    background: #FFD814;
    border-color: #FCD200;
}

.a-button-span12 {
    width: 100% !important;
}

input, select, textarea {
    color: #0F1111;
}

.a-button-primary {
    background: #f2cb68;
    border-color: #a18035;
}

.a-button:not(.a-button-toggle) {
    border-radius: 0px;
    box-shadow: 0 2px 5px 0 rgba(213, 217, 217, .5);
}

.a-button {
    border-radius: 0px;
    border-style: solid;
    border-width: 1px;
    cursor: pointer;
    display: inline-block;
    padding: 0.2rem;
    text-align: center;
    text-decoration: none !important;
    vertical-align: middle;
}
</style>
<script setup>
</script>
