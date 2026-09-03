<!-- <template>
 <main>
 <h1>Tentang Kami</h1>
 <p>Onlineshop ini dikelola oleh siswa SMK Yadika Soreang jurusan
PPLG.</p>
 </main>
</template>
<style scoped>
</style> -->
<script setup>
import { ref } from 'vue'
import TeamCard from '../components/TeamCard.vue'

// Data array anggota tim (Sesuai TODO poin 2)
const daftarTim = ref([
  {
    id: 1,
    nama: 'Resky ganteng',
    jabatan: 'Project Leader',
    inisial: 'R',
    color: '#ff7e5f'
  },
  {
    id: 2,
    nama: 'Fitrah Nur',
    jabatan: 'UI/UX Designer',
    inisial: 'F',
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
  <div class="about-wrapper">
    <!-- Header / Banner Title -->
    <section class="banner-section">
      <h1>Tentang Kami</h1>
    </section>

    <!-- 1. Bagian Cerita Kami (Layout 2 Kolom) -->
    <section class="story-section">
      <div class="story-text">
        <h2>Cerita Kami</h2>
        <p>
          Platform onlineshop ini lahir dari inisiatif mandiri siswa SMK Yadika Soreang jurusan PPLG.
          Fokus utama kami adalah menghadirkan kemudahan bagi seluruh warga sekolah dalam memenuhi
          kebutuhan belajar sehari-hari.
        </p>
        <p>
          Semua produk dikurasi dengan cermat dan terintegrasi langsung dengan sistem pengambilan
          di koperasi sekolah agar praktis dan bebas biaya kirim.
        </p>
      </div>

      <div class="story-image">
        <div class="placeholder-box">
          <img src="data:image/jpeg;base64,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">
        </div>
      </div>
    </section>

    <!-- 2. Bagian Tim Kami (Memanggil TeamCard dengan v-for) -->
    <section class="team-section">
      <h2>Tim Kami</h2>
      <div class="team-grid">
        <!-- Clue: v-for dipanggil berkali-kali -->
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

    <!-- Footer
    <footer class="footer-text">
      © 2026 SMK Yadika Soreang — Onlineshop Sekolah
    </footer> -->
  </div>
</template>

<style scoped>
.about-wrapper {
  font-family: 'Inter', system-ui, -apple-system, sans-serif;
  max-width: 1000px;
  margin: 0 auto;
  padding: 20px;
  color: #2d3748;
}


/* Banner Header */
.banner-section {
   background: linear-gradient(135deg, #2718f1 0%, #e92a2a 100%);
  border-radius: 16px;
  padding: 40px 20px;
  text-align: center;
  color: #ffffff;
  margin-bottom: 40px;
}

.banner-section h1 {
  margin: 0;
  font-size: 1.8rem;
  font-weight: 800;
}

/* 1. Cerita Kami (Clue: display flex, align-items center, gap) */
.story-section {
  display: flex;
  align-items: center;
  gap: 40px;
  margin-bottom: 60px;
  flex-wrap: wrap;
}

/* Clue: flex: 1 supaya 2 kolom berbagi lebar secara merata */
.story-text, .story-image {
  flex: 1;
  min-width: 280px;
}

.story-text h2 {
  font-size: 1.5rem;
  color: #0f172a;
  margin-bottom: 16px;
}

.story-text p {
  font-size: 0.95rem;
  color: #475569;
  line-height: 1.6;
  margin-bottom: 12px;
}

/* Placeholder Gambar Toko */
.placeholder-box {
  background: linear-gradient(135deg, #e2e8f0 0%, #cbd5e1 100%);
  height: 220px;
  border-radius: 16px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #64748b;
  font-weight: 600;
  font-size: 0.9rem;
}

/* 2. Tim Kami */
.team-section {
  text-align: center;
  margin-bottom: 50px;
}

.team-section h2 {
  font-size: 1.5rem;
  color: #0f172a;
  margin-bottom: 30px;
}

.team-grid {
  display: flex;
  justify-content: center;
  gap: 24px;
  flex-wrap: wrap;
}

/* Footer
.footer-text {
  text-align: center;
  font-size: 0.8rem;
  color: #94a3b8;
  padding-top: 20px;
  border-top: 1px solid #e2e8f0;
} */
</style>


