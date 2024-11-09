<template>
    <div class="container mx-auto px-8 pb-12 pt-32">
      <!-- Utakmice i Rezultati -->
      <section class="mb-12">
        <!-- Utakmice i Rezultati sa Flexbox-om -->
        <h2 class="text-3xl font-bold text-center mb-8">Predstojeće Utakmice & Rezultati</h2>
        
        <div class="flex flex-wrap justify-center gap-12"> <!-- Veći gap između blokova -->
          <!-- Utakmica 1 -->
          <div class="bg-white p-6 rounded-lg shadow-md text-center w-full sm:w-1/2 md:w-1/3 mb-8"> <!-- Dodana margina dole -->
            <div class="flex justify-between items-center mb-4">
              <span class="font-semibold">FK Janošik vs. Tim A</span>
              <span class="text-lg text-gray-600">10.12.2024</span>
            </div>
            <img src="https://via.placeholder.com/150" alt="FK Janošik Logo" class="w-full h-32 object-cover mb-4 rounded-md">
            <p class="text-gray-600">Predstojeća utakmica.</p>
            <!-- Dugme ispod utakmice -->
            <div class="mt-6">
              <a href="#" class="bg-blue-500 text-white px-6 py-3 rounded-md font-semibold hover:bg-blue-600 transition">Pogledaj sve utakmice</a>
            </div>
          </div>
  
          <!-- Rezultat 1 -->
          <div class="bg-white p-6 rounded-lg shadow-md text-center w-full sm:w-1/2 md:w-1/3 mb-8"> <!-- Dodana margina dole -->
            <div class="flex justify-between items-center mb-4">
              <span class="font-semibold">FK Janošik vs. Tim X</span>
              <span class="text-lg text-gray-600">02.11.2024</span>
            </div>
            <img src="https://via.placeholder.com/150" alt="FK Janošik Logo" class="w-full h-32 object-cover mb-4 rounded-md">
            <p class="text-gray-600">Rezultat: 2-1 za FK Janošik</p>
            <!-- Dugme ispod rezultata -->
            <div class="mt-6">
              <a href="#" class="bg-blue-500 text-white px-6 py-3 rounded-md font-semibold hover:bg-blue-600 transition">Pogledaj sve rezultate</a>
            </div>
          </div>
        </div>
      </section>
    </div>
  </template>
  