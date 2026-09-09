<script setup>
defineProps({
  title: String,
  image: String,
  description: String,
})
</script>

<template>
  <div
    class="group flex h-full flex-col overflow-hidden rounded-2xl border border-sky-100 bg-white shadow-sm transition duration-100 hover:-translate-y-1 hover:shadow-lg hover:shadow-sky-100/70"
  >

    <div class="overflow-hidden">
      <img
        class="h-48 w-full object-cover transition duration-500 group-hover:scale-105"
        :src="image"
        :alt="title"
      />
    </div>

    <div class="flex flex-1 flex-col gap-3 p-6">

      <h2 class="text-lg font-bold text-slate-800">
        {{ title }}
      </h2>

      <div class="h-1 w-10 rounded-full bg-blue-300"></div>

      <p class="text-sm leading-relaxed text-slate-600">
        {{ description }}
      </p>

      <button
        class="mt-auto w-max rounded-lg bg-blue-300 px-4 py-2 text-sm font-medium text-white transition hover:bg-blue-400"
      >
        Cek Detail
      </button>

    </div>
  </div>
</template>