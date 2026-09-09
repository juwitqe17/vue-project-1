<script setup>
    import { ref } from 'vue';

    const isOpen = ref(false)
    const toggleMenu = () => {
        isOpen.value = !isOpen.value
    }
</script>

<template>
    <section id="home">
        <nav class=" bg-white border-b shadow-md px-12 py-4 flex items-center justify-between">
            <div class="text-2xl font-bold text-gray-800">Jejak Airlangga</div>
            <div class="hidden md:flex gap-6">
                <a href="#home" class="text-gray-600 hover:text-blue-600">Home</a>
                <a href="#mythology" class="text-gray-600 hover:text-blue-600">Mythology</a>
                <a href="#contact" class="text-gray-600 hover:text-blue-600">Contact</a>
            </div>

            <button @click="toggleMenu" class="md:hidden text-gray-600 focus:outline-none">
                <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" fill="none" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"/>
                </svg>
            </button>

        </nav>
            <div v-if="isOpen" class="md:hidden bg-white shadow-md pt-3 px-4 pb-4 space-x-2">
                <a href="#home" class="block text-gray-600 hover:text-blue-600">Home</a>
                <a href="#mythology" class="block text-gray-600 hover:text-blue-600">Mythology</a>
                <a href="#contact" class="block text-gray-600 hover:text-blue-600">Contact</a>
            </div>        
    </section>
    
</template>