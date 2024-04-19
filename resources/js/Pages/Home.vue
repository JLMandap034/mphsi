<script setup>
import { Head } from '@inertiajs/vue3';
import Navbar from '../Layouts/Navbar.vue';

</script>

<template>
    <Head title="Home" />
    <div id="page-body">
        <div class="page-gradient"></div>
        <img id="background" class="top-0" src="/images/bg.jpg"/>
    </div>
    
    <div class="relative min-h-screen flex flex-col">
        <div class="relative w-full" style="padding: 0 5rem 0 5rem">
            <Navbar />
        </div>
    </div>
</template>