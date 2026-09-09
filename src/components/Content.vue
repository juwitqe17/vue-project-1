<script setup>
import Card from './Card.vue';
import Gallery from './Gallery.vue';

const sejarah = [
  {
    nomor: '01',
    judul: 'Gunung Suci Penanggungan',
    deskripsi: 'Candi Belahan berada di lereng Gunung Penanggungan yang dianggap sebagai tempat suci.'
  },
  {
    nomor: '02',
    judul: 'Monumen Pemuliaan Raja',
    deskripsi: 'Candi Belahan menjadi bagian dari peninggalan yang berkaitan dengan pemuliaan Raja Airlangga.'
  },
  {
    nomor: '03',
    judul: 'Warisan Spiritual & Budaya',
    deskripsi: 'Candi Belahan menjadi warisan budaya yang menggambarkan hubungan antara raja, dewa, dan alam semesta.'
  }
]
</script>

<template>
  <section id="history" class="relative overflow-hidden bg-sky-50 px-6 pb-24 pt-32 md:px-12 lg:px-20">

    <div class="pointer-events-none absolute -left-20 top-20 h-64 w-64 rounded-full bg-sky-100/60 blur-3xl"></div>
    <div class="pointer-events-none absolute -right-20 bottom-0 h-72 w-72 rounded-full bg-blue-100/50 blur-3xl"></div>

    <div class="relative mx-auto grid max-w-7xl items-center gap-14 md:grid-cols-2 lg:gap-20">

      <div class="">
        <Gallery />
      </div>

      <div class="flex flex-col gap-8">

        <div class="space-y-4">
          <div class="flex items-center gap-3">
            <span class="h-px w-10 bg-blue-300"></span>
            <span class="text-sm font-semibold uppercase tracking-[0.2em] text-blue-400">
              Sejarah Kahuripan
            </span>
          </div>

          <h1 class="text-4xl font-bold leading-tight text-blue-300 md:text-5xl">
            Jejak Kejayaan Kahuripan
          </h1>

          <p class="max-w-xl leading-relaxed text-slate-600">
            Didirikan oleh Raja Airlangga pada tahun 1019 M, Kerajaan Kahuripan
            tumbuh menjadi pusat peradaban dan kemakmuran di Jawa Timur.
          </p>
        </div>

        <div class="h-px w-full bg-sky-200"></div>

        <div class="flex flex-col gap-4">

          <div
            v-for="item in sejarah"
            :key="item.nomor"
            class="group rounded-2xl border border-sky-100 bg-white p-5 shadow-sm transition duration-300 hover:-translate-y-1 hover:shadow-lg hover:shadow-sky-100/70"
          >
            <div class="flex gap-5">

              <div class="flex h-11 w-11 shrink-0 items-center justify-center rounded-full bg-sky-50 text-sm font-bold text-blue-300 transition group-hover:bg-blue-300 group-hover:text-white">
                {{ item.nomor }}
              </div>

              <div class="flex-1">
                <h2 class="text-lg font-bold text-slate-800">
                  {{ item.judul }}
                </h2>

                <p class="mt-2 text-sm leading-relaxed text-slate-600">
                  {{ item.deskripsi }}
                </p>
              </div>

            </div>
          </div>

        </div>

      </div>
    </div>
  </section>


  <section id="mythology" class="relative overflow-hidden bg-sky-50 px-6 pb-50 pt-20 md:px-12 lg:px-20">

    <div class="pointer-events-none absolute -left-24 top-10 h-64 w-64 rounded-full bg-blue-100/40 blur-3xl"></div>
    <div class="pointer-events-none absolute -right-24 bottom-0 h-72 w-72 rounded-full bg-sky-100/60 blur-3xl"></div>

    <div class="relative mx-auto max-w-7xl flex flex-col gap-12">

      <div class="mb-12 flex flex-col items-center text-center gap-4">

        <div class="mb-4 flex items-center gap-3">
          <span class="h-px w-10 bg-blue-300"></span>

          <span class="text-sm font-semibold uppercase tracking-[0.2em] text-blue-400">
            Mengenal Peninggalan
          </span>

          <span class="h-px w-10 bg-blue-300"></span>
        </div>

        <h1 class="text-4xl font-bold text-blue-300 md:text-5xl">
          Mitologi yang Ada
        </h1>

        <p class="mt-4 max-w-xl text-slate-600">
          Mengenal kisah dan peninggalan yang menjadi bagian dari warisan budaya Kahuripan.
        </p>

      </div>

      <div class="grid gap-6 sm:grid-cols-2 lg:grid-cols-4">

        <Card
          title="Dewi Laksmi"
          image="/dewi_laksmi.jpg"
          description="Di sisi kiri dari dua relung besar di dinding berat Petirtaan Belahan ..."
        />

        <Card
          title="Dewi Sri"
          image="/dewi_sri.jpg"
          description="DI sisi kanan relung besar Petirtaan Belahan, berdiri arca Dewi Sri ..."
        />

        <Card
          title="Relief Kala Menelan Bulan"
          image="/kala_menelan.jpg"
          description="Di depan Petirtaan Belahan terdapat sebuah batu pipih yang menonjol ..."
        />

        <Card
          title="Arca Wisnu"
          image="/arca_wisnu.jpeg"
          description="Arca utama adalah arca Wisnu yang menunggang Garuda ..."
        />

      </div>

    </div>
  </section>
</template>