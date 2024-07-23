<script setup>
import GuestLayout from '@/Layouts/GuestLayout.vue';
import InputError from '@/Components/InputError.vue';
import InputLabel from '@/Components/InputLabel.vue';
import PrimaryButton from '@/Components/PrimaryButton.vue';
import PrimaryButtonAmazon from '@/Components/PrimaryButtonAmazon.vue';
import TextInput from '@/Components/TextInput.vue';
import { Head, Link, useForm } from '@inertiajs/vue3';

const form = useForm({
    name: '',
    email: '',
    password: '',
    password_confirmation: '',
});

const submit = () => {
    form.post(route('register'), {
        onFinish: () => form.reset('password', 'password_confirmation'),
    });
};
</script>

<template>
    <GuestLayout>
        <Head title="Register" />
        <h1 class="font-bold w-48">Crear Cuenta</h1>

        <form @submit.prevent="submit">
            <div class="mt-4">
                <InputLabel for="name" value="Tu nombre" />

                <TextInput
                    id="name"
                    type="text"
                    class="mt-1 block w-full"
                    v-model="form.name"
                    required
                    autofocus
                    autocomplete="name"
                />

                <InputError class="mt-2" :message="form.errors.name" />
            </div>

            <div class="mt-4">
                <InputLabel for="email" value="Correo electronico" />

                <TextInput
                    id="email"
                    type="email"
                    class="mt-1 block w-full"
                    v-model="form.email"
                    required
                    autocomplete="username"
                />

                <InputError class="mt-2" :message="form.errors.email" />
            </div>

            <div class="mt-4">
                <InputLabel for="password" value="Tu contraseña" />

                <TextInput
                    id="password"
                    type="password"
                    class="mt-1 block w-full"
                    v-model="form.password"
                    required
                    autocomplete="new-password"
                    placeholder="debe tener al menos 6 caracteres"
                />
                <div class="input-info">
                    <span class="icon">!</span>
                    <span class="info-text">Minimo 6 caracteres</span>
                </div>

                <InputError class="mt-2" :message="form.errors.password" />
            </div>

            <div class="mt-4">
                <InputLabel for="password_confirmation" value="Vuelve a repetir la contraseña" />

                <TextInput
                    id="password_confirmation"
                    type="password"
                    class="mt-1 block w-full"
                    v-model="form.password_confirmation"
                    required
                    autocomplete="new-password"
                />

                <InputError class="mt-2" :message="form.errors.password_confirmation" />
            </div>
            <div class="flex items-center justify-end mt-4">
                <PrimaryButtonAmazon>
                    Crear una cuenta de Amazon
                </PrimaryButtonAmazon>
            </div>
            <hr class="opacity-0"/>
            <p>Al crear cuenta, aceptas las <a href="" class="text-blue-500">condiciones de uso</a> y el <a href="" class="text-blue-500">Aviso de privacidad de Amazon</a></p>
            <hr class=""/>
            <div class="flex items-center justify-end mt-4">
                <p class="p-2">¿Ya tienes una cuenta?</p>
                <Link
                    :href="route('login')"
                    class="text-blue-500 underline text-sm hover:text-gray-900 rounded-md focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500"
                >
                    Iniciar sesión >
                </Link>
            </div>
        </form>
    </GuestLayout>
</template>

<style>
h1.font-bold {
    font-size: 2rem;
    font-weight: 100;
}

.icon {
    display: inline-block;
    width: 1rem;
    height: 1rem;
    margin-right: 0.25rem;
    background-color: #00b7ff; /* Color del ícono */
    color: #333; /* Color del texto del ícono */
    text-align: center;
    line-height: 1rem;
    border-radius: 50%;
    font-weight: bold;
}

.info-text {
    font-size: 0.8rem;
}

hr {
    border: none;
    width: 76%;
    height: 44px;
    border-bottom: 0px solid #1f120970;
    box-shadow: 0 15px 26px -20px #333;
    margin: 0 auto 0;
}
</style>
