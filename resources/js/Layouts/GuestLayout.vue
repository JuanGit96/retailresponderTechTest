<script setup>
import ApplicationLogo from '@/Components/ApplicationLogo.vue';
import ApplicationLogoAmazon from '@/Components/ApplicationLogoAmazon.vue';
import { Link } from '@inertiajs/vue3';
</script>

<template>
    <div class="min-h-screen flex flex-col sm:justify-center items-center pt-6 sm:pt-0 .bg-white">
        <div>
            <Link href="/">
                <ApplicationLogoAmazon class="w-20 h-20 fill-current text-gray-500" />
            </Link>
        </div>

        <div
            class="w-full sm:max-w-md mt-0 px-6 py-4 bg-white shadow-md overflow-hidden sm:rounded-lg"
        >
            <slot />
        </div>
    </div>
</template>

<script>
window.addEventListener('beforeunload', (event) => {
    console.log('Page is unloading');
});
</script>


<style>
.rounded-md {
    border-radius: 0;
}

input {
    padding-bottom: 0.3rem !important;
    padding-top: 0.3rem !important;
}

.bg-white {
    --tw-bg-opacity: 1;
    background-color: rgb(255 255 255 / var(--tw-bg-opacity));
    border: 1px solid #332e2e45 !important;
}

.focus\:ring-indigo-500:focus {
    --tw-ring-opacity: 1;
    --tw-ring-color: #f2cb68;
}
.focus\:border-indigo-500:focus {
 --tw-border-opacity: 1;
 border-color: #a18035;
}
</style>
