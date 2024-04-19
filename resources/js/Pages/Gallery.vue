<script setup>
import { ref } from 'vue';
import { Head } from '@inertiajs/vue3';
import Navbar from '../Layouts/Navbar.vue';

let shown = ref(false);

const toggleShowGallery = () => {
    shown.value = !shown.value;
};
</script>

<template>
    <Head title="Gallery" />
    <div id="page-body">
        <div class="page-gradient"></div>
        <img id="background" class="top-0" src="/images/bg.jpg"/>
    </div>
    
    <div class="relative min-h-screen flex flex-col">
        <div class="relative w-full" style="padding: 0 5rem 0 5rem">
            <Navbar />
            <div class="grid grid-cols-1 mt-6 mb-12 text-center">
                <div class="card">
                    <label class="gallery-year">2024</label>
                </div>
            </div>
            
            <div class="grid gap-24 grid-cols-3 mt-6 mb-12 text-center">
                <div class="card">
                    <div class="card-body">
                        <div class="mb-6">
                            <label class="gallery-title">FOUNDATION DAY</label>
                            <p class="gallery-date">JANUARY</p>
                        </div>

                        <button type="button" @click="toggleShowGallery" class="btn-primary">View Photos ></button>
                    </div>
                </div>
                
                <div class="card">
                    <div class="card-body">
                        <div class="mb-6">
                            <label class="gallery-title">JS PROM</label>
                            <p class="gallery-date">FEBRURAY</p>
                        </div>

                        <button type="button" @click="toggleShowGallery" class="btn-primary">View Photos ></button>
                    </div>
                </div>
                
                <div class="card">
                    <div class="card-body">
                        <div class="mb-6">
                            <label class="gallery-title">GRADUATION DAY</label>
                            <p class="gallery-date">MARCH</p>
                        </div>

                        <button type="button" @click="toggleShowGallery" class="btn-primary">View Photos ></button>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <Transition name="fade">
        <div v-if="shown.valueOf()" @click="toggleShowGallery" class="gallery-modal-background"></div>
    </Transition>
    <Transition name="fade">
        <div class="gallery-body">
            <div v-if="shown.valueOf()" class="card text-center">
                <div class="card-body">
                    <div class="mb-6">
                        <label class="gallery-title">GRADUATION DAY</label>
                        <p class="gallery-description mb-4 mt-4">
                            Lorem Ipsum is simply dummy text of the printing and typesetting industry.
                            <br>
                            Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged.
                            <br>
                            It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
                        </p>
                    </div>

                    <div class="my-6 grid grid-cols-5 gallery-carousel">
                        <p class="vertical-center"><</p>
                        <img class="gallery-image col-span-3" src="/images/gallery/foundation-day/1.png">
                        <img class="gallery-image col-span-3 active" src="/images/gallery/foundation-day/2.png">
                        <p class="vertical-center">></p>
                    </div>

                    <div>
                        <p class="gallery-pagination"># / 1</p>
                    </div>
                </div>
            </div>
        </div>
        <!-- <div v-if="shown.valueOf()" class="gallery-body text-center">
        </div> -->
    </Transition>
</template>