<script setup>
import { ref } from 'vue'
import TeamCard from '../components/TeamCard.vue'

const daftarTim = ref([
  {
    id: 1,
    nama: 'Resky Gemoy',
    jabatan: 'Project Leader',
    inisial: 'RG',
    color: '#ff6b5f'
  },
  {
    id: 2,
    nama: 'Fitrah Nur',
    jabatan: 'UI/UX Designer',
    inisial: 'FN',
    color: '#159a91'
  },
  {
    id: 3,
    nama: 'Afgan Gembul',
    jabatan: 'Fullstack Dev',
    inisial: 'AG',
    color: '#3b82f6'
  }
])
</script>

<template>
  <div class="min-h-screen bg-white text-slate-800">

    <section
      class="bg-gradient-to-r from-indigo-600 via-purple-500 to-pink-500 p-12 text-center"
    >
      <h1 class="text-4xl font-bold text-white">
        Tentang Kami
      </h1>

      <p class="mt-3 text-white">
        kalian bisa kenalan dengan tim kami 👋
      </p>
    </section>

    <section class="mx-auto max-w-5xl p-6">

      <div class="grid gap-8 md:grid-cols-2">

        <div class="py-4">

          <h2 class="mb-4 text-3xl font-bold text-slate-800">
            Cerita Kami
          </h2>

          <p class="mb-4 leading-7 text-slate-600">
            Platform onlineshop ini lahir dari inisiatif mandiri seorang 
            siswa SMK Yadika Soreang jurusan PPLG.
          </p>

          <p class="leading-7 text-slate-600">
            Fokus utama kami adalah memberikan kemudahan bagi
            warga sekolah dalam memenuhi kebutuhan belajar ngoding dan lain lain .
          </p>

        </div>
      </div>

    </section>
          <div>
  <img
    src="/semangat.jpg"
    alt="Semangat"
    class="h-64 w-full rounded-xl object-cover shadow-lg justify-center"
  />
</div>

    <section class="bg-slate-50 p-8">

      <h2 class="mb-2 text-center text-3xl font-bold">
        Tim Kami
      </h2>

      <p class="mb-8 text-center text-slate-500">
        Orang-orang di balik pembuatan website ini
      </p>


      <div
        class="mx-auto grid max-w-5xl gap-6 md:grid-cols-3"
      >

        <TeamCard
          v-for="anggota in daftarTim"
          :key="anggota.id"
          :nama="anggota.nama"
          :jabatan="anggota.jabatan"
          :inisial="anggota.inisial"
          :bg-color="anggota.color"
        />

      </div>

    </section>


  </div>
</template>
