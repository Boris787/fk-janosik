<script setup lang="ts">
const products = [
  { name: "Zimski duks", sizes: ["XS", "S", "M", "L", "XL", "XXL", "XXXL"], delivery: "7-10 R.dana", price: "2600 RSD", image: "/duks-kapuljaca.png" },
  { name: "Eskimo kapa", sizes: ["Jedna veličina"], delivery: "7-10 R.dana", price: "1000 RSD", image: "/eskimo-kapa.png" },
  { name: "Duks sa rajferslusom", sizes: ["XS", "S", "M", "L", "XL", "XXL", "XXXL"], delivery: "7-10 R.dana", price: "3000 RSD", image: "/duks-rajf.png" },
  { name: "Fk Janošik Šal", sizes: ["Jedna veličina"], delivery: "7-10 R.dana", price: "1800 RSD", image: "/sal.png" },
  { name: "Fk Janošik Hemijske", sizes: ["3 komada"], delivery: "7-10 R.dana", price: "35 RSD", image: "/hemijske.png" },
  { name: "Otvarač Flaša", sizes: ["1 komad"], delivery: "5-7 R.dana", price: "240 RSD", image: "/otvarac.png" }
];
</script>

<template>
  <!-- Header Section -->
  <header class="w-full bg-blue-800 text-white min-h-[500px] flex items-center font-lato">
    <div class="container mx-auto px-8 py-20 text-center">
      <img src="/public/fkjanosik-logo.png" alt="FK Janosik Logo" class="w-24 mx-auto mb-4">
      <h1 class="text-4xl md:text-5xl font-bold">Dobrodošli u FK Janošik Merch</h1>
      <p class="text-lg mt-4 mb-8">
        100% pamuk, udoban za zimsko vreme. Pronađite kvalitetnu opremu za podršku vašem omiljenom klubu!
      </p>
    </div>
  </header>

  <!-- Products Section -->
  <section class="container mx-auto px-8 py-12">
    <h2 class="text-3xl font-bold text-center mb-8">Naša Kolekcija</h2>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-8">
      <!-- Product Card -->
      <div v-for="(product, index) in products" :key="index" class="bg-white p-6 rounded-lg shadow-lg text-center hover:shadow-xl transition-all duration-300 ease-in-out">
        <!-- Price Section -->
        <div class="text-xl font-semibold text-blue-800 mb-2">{{ product.price }}</div>
        
        <!-- Product Image -->
        <img :src="product.image" :alt="`Slika ${product.name}`" class="w-full h-48 object-cover mb-4 rounded-md transition-transform transform hover:scale-105 duration-300">
        
        <!-- Product Name -->
        <h3 class="text-xl font-semibold text-gray-800 mb-2">{{ product.name }}</h3>
        
        <!-- Sizes Section -->
        <p class="text-sm text-gray-600 mb-4">Veličine: {{ product.sizes.join(", ") }}</p>
        
        <!-- Delivery Section -->
        <p class="text-sm text-gray-600 mb-4">Rok isporuke: {{ product.delivery }}</p>
        
        <!-- Buy Button -->
        <a href="#" class="inline-block bg-yellow-500 text-white px-6 py-3 rounded-md font-semibold hover:bg-yellow-600 transition-all duration-300 ease-in-out">
          Poručite odmah
        </a>
      </div>
    </div>
  </section>
</template>

<style scoped>
header {
  background-image: url('/public/background-texture.png'); /* Dodaj teksturu pozadine po želji */
  background-size: cover;
  background-position: center;
}

.product-card {
  border-radius: 15px;
  overflow: hidden;
}

.product-card:hover {
  transform: translateY(-10px);
}

.product-price {
  font-size: 1.25rem;
  color: #2c3e50;
}

.product-name {
  font-size: 1.2rem;
  font-weight: bold;
  color: #34495e;
}

.product-button {
  padding: 12px 20px;
  background-color: #f39c12;
  color: white;
  font-weight: bold;
  border-radius: 8px;
  transition: all 0.3s ease;
}

.product-button:hover {
  background-color: #e67e22;
  transform: scale(1.05);
}

.product-image:hover {
  transform: scale(1.05);
}
</style>
