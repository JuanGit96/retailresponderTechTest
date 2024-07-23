<template>
<span id="continue" class="a-button a-button-span12 a-button-primary">
    <span class="a-button-inner">
        <button id="continue-announce" class="a-button-text" aria-hidden="true">
              <slot />
        </button>
    </span>
</span>


</template>
<style>
.a-button {
    background: #e7e9ec;
    border-radius: 3px;
    border-color: #adb1b8 #a2a6ac #8d9096;
    border-style: solid;
    border-width: 1px;
    cursor: pointer;
    display: inline-block;
    padding: 0;
    text-align: center;
    text-decoration: none !important;
    vertical-align: middle;
}

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
    background: #FFD814;
    border-color: #FCD200;
}

.a-button:not(.a-button-toggle) {
    border-radius: 8px;
    box-shadow: 0 2px 5px 0 rgba(213, 217, 217, .5);
}

.a-button {
    border-radius: 3px;
    border-style: solid;
    border-width: 1px;
    cursor: pointer;
    display: inline-block;
    padding: 2px;
    text-align: center;
    text-decoration: none !important;
    vertical-align: middle;
}
</style>
<script setup>
</script>
