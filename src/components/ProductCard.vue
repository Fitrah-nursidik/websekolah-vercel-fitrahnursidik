<!-- <script setup>
import { ref } from 'vue'
defineProps(['nama', 'harga', 'gambar'])
const gambarDipilih = ref(null)
function bukaPreview(src) {
 gambarDipilih.value = src
}
function tutupPreview() {
 gambarDipilih.value = null
}
function tambahKeKeranjang(nama) {
 const suara = new Audio('/audio/notifikasi.mp3')
 suara.play()
 alert(`${nama} ditambahkan ke keranjang!`)
}

</script>
<template>
 <div class="card">
 <img :src="gambar" :alt="nama" @click="bukaPreview(gambar)" />
 <h3>{{ nama }}</h3>
 <p>Rp {{ harga.toLocaleString('id-ID') }}</p>
 <button @click="tambahKeKeranjang(nama)">Tambah ke Keranjang</button>
 <div v-if="gambarDipilih" class="preview-overlay" @click="tutupPreview">
<img :src="gambarDipilih" class="preview-besar" />
<button @click="Tutup(nama)">Tutup</button>
 </div>
</div>
</template>
<style scoped>
.card {
 border: 1px solid #ddd;
 border-radius: 10px;
 padding: 14px;
 width: 200px;
 text-align: center;
  background: linear-gradient(135deg, #2718f1 0%, #e92a2a 100%);
}
.card img { width: 100%; border-radius: 6px; cursor: pointer; }
.preview-overlay {
 position: fixed; top: 0; left: 0; width: 100%; height: 100%;
 background: rgba(0, 0, 0, 0.7);
 display: flex; align-items: center; justify-content: center;
 cursor: zoom-out;
}
.preview-besar { max-width: 80%; max-height: 80%; border-radius: 8px; }

button {
 margin-top: 8px;
 padding: 6px 12px;
 border: none;
 border-radius: 10px;
 background: #0a0a0a;
 color: rgb(230, 236, 235);
 cursor: pointer;
}
button:hover { background: #2bc08e; }
</style> -->
<script setup>
import { ref } from 'vue'
defineProps(['nama', 'harga', 'gambar'])
const gambarDipilih = ref(null)
function bukaPreview(src) {
 gambarDipilih.value = src
}
function tutupPreview() {
 gambarDipilih.value = null
}
function tambahKeKeranjang(nama) {
 const suara = new Audio('/audio/notifikasi.mp3')
 suara.play()
 alert(`${nama} ditambahkan ke keranjang!`)
}
</script>
<template>
 <div class="bg-white rounded-xl shadow-md p-4 hover:shadow-lg transition">
 <img :src="gambar" :alt="nama" @click="bukaPreview(gambar)"
 class="w-full h-40 object-cover rounded-lg cursor-pointer" />
 <h3 class="text-lg font-semibold mt-2">{{ nama }}</h3>
 <p class="text-gray-600">Rp {{ harga.toLocaleString('id-ID') }}</p>
 <button @click="tambahKeKeranjang(nama)"
 class="bg-blue-600 text-white px-4 py-2 rounded-lg mt-2 w-full hover:bgblue-700">
 Tambah ke Keranjang
 </button>
 </div>
 <div v-if="gambarDipilih" class="fixed inset-0 bg-black/70 flex items-center justifycenter cursor-zoom-out"
 @click="tutupPreview">
 <img :src="gambarDipilih" class="max-w-[80%] max-h-[80%] rounded-lg" />
 </div>
</template>