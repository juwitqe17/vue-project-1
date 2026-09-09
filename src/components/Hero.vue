<script setup>
    import { ref } from 'vue';
    function handleClick() {
        alert('Coba aja sih')
    }
</script>

<template>
    <section>
        <div class="relative h-screen bg-cover bg-center " style="background-image: url('/public/petirtaan_belahan.jpg')">
            <div class="absolute inset-0 bg-black/50"></div>

            <div class="relative z-10 flex h-full flex-col items-center justify-center px-4 text-center text-white gap-5 transition duration-100">
                
                <h class="text-5xl font-black">
                    Petirtaan Suci Warisan Raja Airlangga dan Para Dewi
                </h>
                <p class="text-xl mt-3">
                    Jelajahi jejak sejarah dan keagungan Raja Airlangga melalui pengalaman eksplorasi berbasis web yang menyenangkan.
                </p>
                <button class="bg-gray-500 rounded-md p-2 text-white transition hover:text-gray-600 hover:bg-white" @click="handleClick">
                    Jelajahi Mitologi
                </button>

            </div>

            <div class="absolute bottom-0 left-1/2 -translate-x-1/2 translate-y-1/2 w-11/12 max-w-6xl bg-white p-7 rounded-xl shadow-lg z-10">
                <p class="text-center text-lg text-gray-700">Di lereng timur Gunung Penanggungan, sebuah gunung yang sejak masa Hindu-Buddha dianggap suci, berdiri sebuah situs unik bernama Petirtaan Belahan atau yang sering disebut Candi Belahan. Situs ini tidak berbentuk candi menjulang seperti Prambanan, melainkan berupa pemandian suci (pertirtaan) yang masih dialiri air hingga kini.</p>
            </div>
        </div>    
    </section>

</template>