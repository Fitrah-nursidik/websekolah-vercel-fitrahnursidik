<template>
  <div class="contact-page">
    <!-- Banner Header -->
    <div class="hero-banner">
      <h1>Hubungi Kami</h1>
    </div>

    <!-- Main Content Container -->
    <div class="contact-container">
      <!-- Bagian Kiri: Info Kontak -->
      <div class="info-section">
        <h2>Info Kontak</h2>
        
        <div class="info-item">
          <p class="info-label">📍 Alamat</p>
          <p class="info-value">Jl. dinya No. 1, Soreang, Kab. Bandung meren</p>
        </div>

        <div class="info-item">
          <p class="info-label">📞 Telepon</p>
          <p class="info-value">(+62)85759211781</p>
        </div>

        <div class="info-item">
          <p class="info-label">✉️ Email</p>
          <p class="info-value">FitrahNursidikOnlineshop@gmail.com</p>
        </div>
      </div>

      <!-- Bagian Kanan: Formulir -->
      <div class="form-card">
        <h3>Kirim Pesan</h3>
        <form @submit.prevent>
          <div class="form-group">
            <label for="nama">Nama</label>
            <input type="text" id="nama" placeholder="Nama kamu" />
          </div>

          <div class="form-group">
            <label for="email">Email</label>
            <input type="email" id="email" placeholder="email@contoh.com" />
          </div>

          <div class="form-group">
            <label for="pesan">Pesan</label>
            <textarea id="pesan" rows="4" placeholder="Tulis pesan..."></textarea>
          </div>

          <button type="button" class="btn-submit">Kirim</button>
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

<style scoped>
.contact-page {
  font-family: Arial, sans-serif;
  color: #333;
}

/* Banner Biru */
.hero-banner {
 background: linear-gradient(135deg, #2718f1 0%, #e92a2a 100%);
  color: white;
  text-align: center;
  padding: 40px 20px;
  margin-bottom: 40px;
}

.hero-banner h1 {
  margin: 0;
  font-size: 2rem;
  font-weight: bold;
}

/* Container 2 Kolom */
.contact-container {
  display: flex;
  gap: 40px;
  max-width: 900px;
  margin: 0 auto 50px auto;
  padding: 0 20px;
  justify-content: space-between;
}

/* Kolom Kiri - Info Kontak */
.info-section {
  flex: 1;
}

.info-section h2 {
  font-size: 1.5rem;
  margin-bottom: 24px;
}

.info-item {
  margin-bottom: 20px;
}

.info-label {
  font-weight: bold;
  margin-bottom: 4px;
  display: flex;
  align-items: center;
  gap: 6px;
}

.info-value {
  margin: 0;
  color: #666;
  font-size: 0.95rem;
  padding-left: 24px;
}

/* Kolom Kanan - Kartu Formulir */
.form-card {
  flex: 1;
  background-color: #f8f9fa;
  padding: 30px;
  border-radius: 16px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.03);
}

.form-card h3 {
  margin-top: 0;
  margin-bottom: 20px;
  font-size: 1.25rem;
}

.form-group {
  margin-bottom: 16px;
}

.form-group label {
  display: block;
  font-size: 0.85rem;
  font-weight: 600;
  margin-bottom: 6px;
  color: #444;
}

.form-group input,
.form-group textarea {
  width: 100%;
  padding: 10px 14px;
  border: 1px solid #e0e0e0;
  border-radius: 8px;
  font-size: 0.9rem;
  outline: none;
  box-sizing: border-box;
  background-color: #fff;
}

.form-group input:focus,
.form-group textarea:focus {
  border-color: #4f46e5;
}

/* Tombol Kirim Berbentuk Pil */
.btn-submit {
  background-color: #4f46e5;
  color: white;
  border: none;
  padding: 10px 28px;
  border-radius: 999px;
  font-weight: 600;
  cursor: pointer;
  font-size: 0.9rem;
  transition: background-color 0.2s;
}

.btn-submit:hover {
  background-color: #4338ca;
}

/* Responsif untuk layar HP */
@media (max-width: 640px) {
  .contact-container {
    flex-direction: column;
    gap: 30px;
  }
}
</style>
