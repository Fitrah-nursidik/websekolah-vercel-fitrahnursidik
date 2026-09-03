<template>
  <!-- <div class="landing-page"> -->
    <!-- <section class="hero"> -->
      <div class="hero bg-cyan-500 p-[100px] flex flex-col items-center justify-center text-white gap-[18px] ">
      <h1 class="text-[25pt] text-center">Belanja Perlengkapan Buat Main Game atau Belajar, Gampang & Terpercaya</h1>
      <p class="text-[20pt] landing-[80pt]">Dari pc, laptop, sampai monitor — semua ada di satu tempat.</p>
      <!-- <RouterLink to="/product" class="btn-hero">Lihat Produk</RouterLink> -->
       <RouterLink to="/product" button class="text-[10pt] bg-white text-black p-[10px] rounded-full font-bold animate-pulse 
       display: inline-block;">Lihat produk</RouterLink>
      </div>
    <!-- </section> -->
<video controls width="480" muted loop>
 <source src="https://www.w3schools.com/html/mov_bbb.mp4" type="video/mp4" />
 Browser kamu tidak mendukung pemutaran video.
</video>
    <!-- Bagian Fitur (Menggunakan Props) -->
    <section class="inline-flex flex-wrap gap-[20px] justify-center scroll-ml-6 p-[150px] ">
      <FeatureCard 
        icon="🏷️" 
        title="Kualitas Terjamin" 
        description="Bahan dipilih langsung oleh tim terbaik." 
      />
      <FeatureCard 
        icon="💰" 
        title="Harga Bersahabat" 
        description="Harga ramah di kantong." 
      />
      <FeatureCard 
        icon="🏫" 
        title="Ambil di tempat" 
        description="Tidak perlu ongkir, ambil di koperasi." 
      />
    </section>
</template>

<script setup>
import FeatureCard from '../components/FeatureCard.vue'
</script>

<!-- <style scoped>
/* Style Bagian Hero */
.hero {
   background: linear-gradient(135deg, #2718f1 0%, #e92a2a 100%);
  color: white;
  padding: 60px 20px;
  text-align: center;
}

.hero h1 {
  font-size: 2rem;
  margin-bottom: 12px;
}

.hero p {
  margin-bottom: 24px;
  opacity: 0.9;
}

.btn-hero {
  display: inline-block;
  background-color: white;
  color: #4f46e5;
  padding: 10px 24px;
  border-radius: 999px;
  text-decoration: none;
  font-weight: bold;
  transition: transform 0.2s;
}

.btn-hero:hover {
  transform: translateY(-2px);
}

/* Container untuk menjajarkan kartu fitur */
.features-container {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  justify-content: center;
  margin-top: 30px;
  padding: 0 20px 40px 20px;
}
video {
 margin-top: 16px;
 border-radius: 10px;
 display: block;
}
</style> -->
