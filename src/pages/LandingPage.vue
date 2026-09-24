<template>

  <section
    class="bg-gradient-to-r from-indigo-600 via-purple-500 to-pink-500
    px-6 py-20 text-center text-white"
  >

    <h1 class="mx-auto max-w-3xl text-3xl font-bold">
      Belanja Perlengkapan Buat Main Game atau Belajar,
      Gampang & Terpercaya
    </h1>

    <p class="mt-5 text-lg">
      Dari PC, laptop, sampai monitor — semua ada di satu tempat.
    </p>

    <RouterLink
      to="/product"
      class="mt-6 inline-block rounded-full bg-white px-6 py-3
      font-bold text-purple-600 hover:bg-gray-100"
    >
      Lihat Produk
    </RouterLink>

  </section>

  <section class="flex justify-center bg-white px-6 py-10">

    <video
      controls
      muted
      loop
      class="w-full max-w-xl rounded-xl shadow-lg"
    >
      <source
        src="https://www.w3schools.com/html/mov_bbb.mp4"
        type="video/mp4"
      />

      Browser kamu tidak mendukung pemutaran video.
    </video>

  </section>


  <section class="bg-slate-50 px-6 py-10">

    <div
      class="mx-auto grid max-w-4xl grid-cols-2 gap-5"
    >

      <FeatureCard
        icon="🏷️"
        title="Kualitas Terjamin,aman dan terpercaya tanpa lecet"
        description="Bahan dipilih langsung oleh tim terbaik kita."
      />
      <FeatureCard
        icon="💰"
        title="Harga Bersahabat banget "
        description="Harga ramah di kantong,aalitan es."
      />

    </div>

    <div class="mx-auto mt-5 max-w-4xl">

      <div class="mx-auto w-1/2 min-w-[160px] grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3">

        <FeatureCard
          icon="🏫"
          title="Ambil di tempat atau koperasi"
          description="Tidak perlu ongkir karna kamu yang datang ke koperasi."
        />

      </div>

    </div>

  </section>

</template>

<script setup>
import FeatureCard from '../components/FeatureCard.vue'
</script>
