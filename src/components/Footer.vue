<script setup>
const tahun = new Date().getFullYear()
</script>
<template>
    <div class="footer">
 <hr />
 <footer>
 <small>&copy; {{ tahun }} FITRAH NURSIDIK — Onlineshop
</small>
 </footer>
 </div>
</template>
<style scoped>
.footer {
  text-align: center;
  padding: 20px;
  font-size: 12px;
  color: #888;
  border-top: 1px solid #eee;
}
</style>
