<template>
  <!-- <div class="atas">
    <nav>
            <h2>Fitrah Nursidik - Onlineshop</h2>
        <RouterLink to="/">Landing</RouterLink> |
        <RouterLink to="/product">Product</RouterLink> |
        <RouterLink to="/about">About</RouterLink> |
        <RouterLink to="/contact">Contact</RouterLink> |
      </nav>
    <hr />
    </div> -->
     <header class="navbar">
      <div class="brand-logo">Fitrah Nursidik — Onlineshop</div>
      <nav class="nav-links">
        <RouterLink to="/" class="nav-item">Landing</RouterLink>
        <RouterLink to="/product" class="nav-item">Product</RouterLink>
        <RouterLink to="/about" class="nav-item ">About</RouterLink>
        <RouterLink to="/contact" class="nav-item">Contact</RouterLink>
      </nav>
    </header>
  <hr />
</template>

<style scoped>
/* .atas{
text-align: center;
}  */
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 0;
  margin-bottom: 20px;
}

.brand-logo {
  font-weight: 700;
  font-size: 0.95rem;
  color: #1a202c;
}

.nav-links {
  display: flex;
  gap: 20px;
}

.nav-item {
  text-decoration: none;
  color: #64748b;
  font-weight: 500;
  font-size: 0.9rem;
}

.nav-item.active, .nav-item:hover {
  color: #0d9488;
  font-weight: 700;
}

</style>