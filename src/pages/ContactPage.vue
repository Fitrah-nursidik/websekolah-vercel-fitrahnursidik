<template>
  <div class="font-sans text-gray-800">
    <!-- Banner Header -->
    <div
      class="mb-10 bg-gradient-to-br from-indigo-600 to-red-500 px-5 py-10 text-center text-white"
    >
      <h1 class="m-0 text-3xl font-bold">
        Hubungi Kami
      </h1>
    </div>

    <!-- Main Content Container -->
    <div
      class="mx-auto mb-12 flex max-w-5xl flex-col gap-8 px-5 md:flex-row md:gap-10"
    >
      <!-- Bagian Kiri: Info Kontak -->
      <div class="flex-1">
        <h2 class="mb-6 text-2xl font-semibold">
          Info Kontak
        </h2>

        <div class="mb-5">
          <p class="mb-1 flex items-center gap-2 font-bold">
            📍 Alamat
          </p>
          <p class="m-0 pl-6 text-sm text-gray-500">
            Jl. dinya No. 1, Soreang, Kab. Bandung meren
          </p>
        </div>

        <div class="mb-5">
          <p class="mb-1 flex items-center gap-2 font-bold">
            📞 Telepon
          </p>
          <p class="m-0 pl-6 text-sm text-gray-500">
            (+62)85759211781
          </p>
        </div>

        <div class="mb-5">
          <p class="mb-1 flex items-center gap-2 font-bold">
            ✉️ Email
          </p>
          <p class="m-0 pl-6 text-sm text-gray-500">
            FitrahNursidikOnlineshop@gmail.com
          </p>
        </div>
      </div>

      <!-- Bagian Kanan: Formulir -->
      <div
        class="flex-1 rounded-2xl bg-gray-50 p-7 shadow-md"
      >
        <h3 class="mb-5 mt-0 text-xl font-semibold">
          Kirim Pesan
        </h3>

        <form @submit.prevent>
          <!-- Nama -->
          <div class="mb-4">
            <label
              for="nama"
              class="mb-1.5 block text-sm font-semibold text-gray-700"
            >
              Nama
            </label>

            <input
              type="text"
              id="nama"
              placeholder="Nama kamu"
              class="box-border w-full rounded-lg border border-gray-200 bg-white px-3.5 py-2.5 text-sm outline-none transition focus:border-indigo-500"
            />
          </div>

          <!-- Email -->
          <div class="mb-4">
            <label
              for="email"
              class="mb-1.5 block text-sm font-semibold text-gray-700"
            >
              Email
            </label>

            <input
              type="email"
              id="email"
              placeholder="email@contoh.com"
              class="box-border w-full rounded-lg border border-gray-200 bg-white px-3.5 py-2.5 text-sm outline-none transition focus:border-indigo-500"
            />
          </div>

          <!-- Pesan -->
          <div class="mb-4">
            <label
              for="pesan"
              class="mb-1.5 block text-sm font-semibold text-gray-700"
            >
              Pesan
            </label>

            <textarea
              id="pesan"
              rows="4"
              placeholder="Tulis pesan..."
              class="box-border w-full resize-y rounded-lg border border-gray-200 bg-white px-3.5 py-2.5 text-sm outline-none transition focus:border-indigo-500"
            ></textarea>
          </div>

          <!-- Tombol -->
          <button
            type="button"
            class="cursor-pointer rounded-full border-0 bg-indigo-600 px-7 py-2.5 text-sm font-semibold text-white transition hover:bg-indigo-700"
          >
            Kirim
          </button>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ContactPage',
}
</script>
