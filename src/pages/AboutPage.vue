<script setup>
import { ref } from 'vue'
import TeamCard from '../components/TeamCard.vue'

const daftarTim = ref([
  {
    id: 1,
    nama: 'Resky Ganteng',
    jabatan: 'Project Leader',
    inisial: 'RG',
    color: '#ff7e5f'
  },
  {
    id: 2,
    nama: 'Fitrah Nur',
    jabatan: 'UI/UX Designer',
    inisial: 'FN',
    color: '#0d9488'
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
  <div class="min-h-screen bg-green-400">

    <!-- Judul -->
    <section class="bg-gradient-to-r from-purple-500 to-pink-500 p-8 text-center">
      <h1 class="text-3xl font-bold">
        Tentang Kami
      </h1>
    </section>


    <!-- Cerita Kami -->
    <section class="mx-auto max-w-5xl p-6">

      <div class="grid gap-6 md:grid-cols-2">

        <!-- Teks -->
        <div class="bg-white rounded-lg p-6">
          <h2 class="mb-3 text-2xl font-bold">
            Cerita Kami
          </h2>

          <p class="mb-3">
            Platform onlineshop ini lahir dari inisiatif mandiri
            siswa SMK Yadika Soreang jurusan PPLG.
          </p>

          <p>
            Fokus utama kami adalah memberikan kemudahan bagi
            warga sekolah dalam memenuhi kebutuhan belajar sehari-hari.
          </p>
        </div>


        <!-- Gambar -->
        <div>
          <img
            src="/images/semangat.jpg"
            alt="Semangat"
            class="h-64 w-full rounded-lg object-cover"
          />
        </div>

      </div>

    </section>


    <!-- Tim Kami -->
    <section class="bg-white p-6">

      <h2 class="mb-6 text-center text-2xl font-bold">
        Tim Kami
      </h2>

      <div class="mx-auto grid max-w-5xl gap-6 md:grid-cols-3">

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


    <!-- Footer -->
    <footer class="bg-white p-5 text-center">
      <p class="text-gray-500">
        © 2026 FITRAH NURSIDIK — Onlineshop
      </p>
    </footer>

  </div>
</template>
