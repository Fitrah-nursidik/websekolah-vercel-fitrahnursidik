<template>
  <div class="feature-card">
    <div class="icon">{{ icon }}</div>
    <h3>{{ title }}</h3>
    <p>{{ description }}</p>
  </div>
</template>

<script setup>
defineProps({
  icon: {
    type: String,
    default: '✨'
  },
  title: {
    type: String,
    required: true
  },
  description: {
    type: String,
    required: true
  }
})
</script>

<style scoped>
.feature-card {
  background-color: #77d1e7;
  padding: 24px;
  border-radius: 12px;
  box-shadow: 0 6px 14px rgba(0, 0, 0, 0.08);
  text-align: center;
  width: 250px;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

/* Efek hover sesuai petunjuk tugas */
.feature-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.12);
}

.icon {
  font-size: 2rem;
  margin-bottom: 8px;
}

h3 {
  margin: 8px 0;
  font-size: 1.1rem;
  color: #1a1a1a;
}

p {
  font-size: 0.9rem;
  color: #666;
  margin: 0;
}
</style>
