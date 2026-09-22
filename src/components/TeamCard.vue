<script setup>
defineProps({
  nama: String,
  jabatan: String,
  inisial: String,
  bgColor: String
})
</script>

<template>

  <div
    class="rounded-xl bg-white p-6 text-center shadow-md"
  >

    <div
      class="mx-auto flex h-20 w-20 items-center justify-center rounded-full text-2xl font-bold text-white"
      :style="{ backgroundColor: bgColor }"
    >
      {{ inisial }}
    </div>

    <h3 class="mt-4 text-xl font-bold text-slate-800">
      {{ nama }}
    </h3>

    <p class="mt-2 text-gray-500">
      {{ jabatan }}
    </p>

  </div>

</template>
