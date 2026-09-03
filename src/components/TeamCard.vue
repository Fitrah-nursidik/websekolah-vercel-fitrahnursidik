<script setup>
// Clue: defineProps dipakai di TeamCard.vue untuk menerima data nama, jabatan, & inisial/warna
defineProps({
  nama: {
    type: String,
    required: true
  },
  jabatan: {
    type: String,
    required: true
  },
  inisial: {
    type: String,
    default: '?'
  },
  bgColor: {
    type: String,
    default: '#0d9488' // Warna default avatar
  }
})
</script>

<template>
  <div class="team-card">
    <!-- Avatar lingkaran dengan inisial -->
    <div class="avatar" :style="{ backgroundColor: bgColor }">
      {{ inisial }}
    </div>
    <h4 class="member-name">{{ nama }}</h4>
    <p class="member-role">{{ jabatan }}</p>
  </div>
</template>

<style scoped>
.team-card {
  background: #ffffff;
  padding: 24px 20px;
  border-radius: 16px;
  text-align: center;
  width: 200px;

  /* Box shadow & efek hover terangkat */
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.05);
  border: 1px solid #f1f5f9;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.team-card:hover {
  transform: translateY(-6px);
  box-shadow: 0 12px 25px rgba(13, 148, 136, 0.15);
}

/* Avatar Lingkaran (Clue: border-radius: 50%) */
.avatar {
  width: 64px;
  height: 64px;
  border-radius: 50%;
  color: #ffffff;
  font-size: 22px;
  font-weight: 700;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 16px auto;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

.member-name {
  font-size: 1rem;
  font-weight: 700;
  color: #1e293b;
  margin-bottom: 4px;
}

.member-role {
  font-size: 0.8rem;
  color: #64748b;
  margin: 0;
}
</style>
