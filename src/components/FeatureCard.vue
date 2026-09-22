<script setup>
defineProps({
  icon: String,
  title: String,
  description: String
})
</script>

<template>

  <div
    class="rounded-xl bg-white p-5 text-center shadow-md"
  >

    <div class="text-3xl">
      {{ icon }}
    </div>

    <h3 class="mt-3 font-bold text-slate-800">
      {{ title }}
    </h3>

    <p class="mt-2 text-sm text-gray-500">
      {{ description }}
    </p>

  </div>

</template>
