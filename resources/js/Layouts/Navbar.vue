<script setup>
import { ref } from 'vue';
import { Link } from '@inertiajs/vue3'

let path = window.location.href;
let shown = ref(false);

const toggleLoginHandler = () => {
    shown.value = !shown.value;
};
</script>

<template>
    <header class="grid">
        <div class="navbar-logo absolute">
            <img class="navbar-icon vertical-center" src="/images/icon.png">
            <span class="navbar-title vertical-center text-white">MPHSI</span>
        </div>
        <nav class="navbar flex flex-1 justify-end">
            <Link
                :href="route('home')"
                :class="{'active': route('home')+'/' === path}"
                class="rounded-md px-3 py-2 text-black ring-1 ring-transparent transition text-white vertical-center"
            >
                HOME
            </Link>
            <Link
                :href="route('about')"
                :class="{'active': route('about') === path}"
                class="rounded-md px-3 py-2 text-black ring-1 ring-transparent transition text-white vertical-center"
            >
                ABOUT
            </Link>
            <Link
                :href="route('gallery')"
                :class="{'active': route('gallery') === path}"
                class="rounded-md px-3 py-2 text-black ring-1 ring-transparent transition text-white vertical-center"
            >
                GALLERY
            </Link>
            <Link
                :href="route('contact-us')"
                :class="{'active': route('contact-us') === path}"
                class="rounded-md px-3 py-2 text-black ring-1 ring-transparent transition text-white vertical-center"
            >
                CONTACT US
            </Link>
            <button
                type="button"
                @click="toggleLoginHandler"
                class="rounded-md px-3 py-2 text-black ring-1 ring-transparent transition vertical-center"
            >
                <img class="user-login vertical-center" src="/images/login.png">
            </button>
        </nav>
    </header>
    
    <!-- LOGIN -->
    <Transition name="fade">
        <div v-if="shown.valueOf()" @click="toggleLoginHandler" class="login-background"></div>
    </Transition>
    <Transition name="slide">
        <div v-if="shown.valueOf()" class="login-body py-6 px-8">
            <div class="mt-14">
                <label class="mb-4" for="email">E-mail</label>
                <input type="text" name="email" id="email">
            </div>
            <div class="mt-4 mb-6">
                <label class="mb-4" for="password">Password</label>
                <input type="password" name="password" id="password">
            </div>

            <div>
                <button type="button" class="btn-danger" @click="toggleLoginHandler">Cancel</button>
                <button type="button" class="btn-primary" style="float: right;">Submit</button>
            </div>
        </div>
    </Transition>
</template>