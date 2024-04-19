<script setup>
import { Head } from '@inertiajs/vue3';
import Navbar from '../Layouts/Navbar.vue';
import TextInput from '../Components/TextInput.vue';
</script>

<template>
    <Head title="Contact Us" />
    <div id="page-body">
        <div class="page-gradient"></div>
        <img id="background" class="top-0" src="/images/bg.jpg"/>
    </div>
    
    <div class="relative min-h-screen flex flex-col">
        <div class="relative w-full" style="padding: 0 5rem 0 5rem">
            <Navbar />

            <div class="grid grid-cols-1 mt-6 mb-12">
                <div class="card">
                    <div class="card-body contact-us">
                        <div class="grid grid-cols-2">
                            <div class="contact-us-details">
                                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3859.1805260005567!2d121.06040607590545!3d14.70238087457509!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3397b0bdc5db686f%3A0x5dedfe790ae0e556!2sMother%20of%20Perpetual%20Help%20School!5e0!3m2!1sen!2sph!4v1713337965394!5m2!1sen!2sph" width="790" height="365" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>

                                <div class="mt-4">
                                    <label>Facebook</label>
                                    <p class="mt-2">Mother of Perpetual Help School Inc.</p>
                                </div>
                                <div class="mt-4">
                                    <label>Twitter</label>
                                    <p class="mt-2">Mother of Perpetual Help School Inc.</p>
                                </div>
                                <div class="mt-4">
                                    <label>E-mail</label>
                                    <p class="mt-2"><u>mphs1990@gmail.com</u></p>
                                </div>
                                <div class="mt-4">
                                    <label>Contact Number</label>
                                    <p class="mt-2"><u>(02) 3430 8209</u></p>
                                </div>
                            </div>
                            <div class="contact-us-form">
                                <div class="mb-4">
                                    <label class="mb-4" for="name">Name</label>
                                    <input type="text" name="name" id="name">
                                </div>
                                
                                <div class="mb-4">
                                    <label class="mb-4" for="email">E-mail</label>
                                    <input type="text" name="email" id="email">
                                </div>
                                
                                <div class="mb-4">
                                    <label class="mb-4" for="contact_number">Contact Number</label>
                                    <input type="text" name="contact_number" id="contact_number">
                                </div>
                                
                                <div class="mb-4">
                                    <label class="mb-4" for="message">Message</label>
                                    <textarea name="message" id="message" rows="10" />
                                </div>

                                <div style="float: right;">
                                    <button type="button" class="btn-primary">Submit</button>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>