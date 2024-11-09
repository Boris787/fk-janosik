<script setup lang="ts"> 

const players = [
  { name: "Mario Halas", age: 22, position: "Levi bek", image: "/mariohalas.png" },
  { name: "Petar Janković", age: 23, position: "Desni bek", image: "/mariohalas.png" },
  { name: "Nemanja Petrović", age: 24, position: "Vezni", image: "/mariohalas.png" },
  { name: "Ivan Milovanović", age: 21, position: "Napadač", image: "/mariohalas.png" },
  { name: "Marko Nikolić", age: 25, position: "Odbrambeni", image: "/mariohalas.png" },
  { name: "Luka Marković", age: 20, position: "Golman", image: "/mariohalas.png" },
  { name: "Aleksandar Simović", age: 27, position: "Vezni", image: "/mariohalas.png" },
  { name: "Stefan Ilić", age: 19, position: "Levi bek", image: "/mariohalas.png" },
  { name: "Nikola Živković", age: 22, position: "Desni bek", image: "/mariohalas.png" },
  { name: "Bojan Perić", age: 23, position: "Napadač", image: "/mariohalas.png" },
  { name: "Miljan Kovačević", age: 24, position: "Vezni", image: "/mariohalas.png" },
  { name: "Marijan Skumpija", age: 45, position: "Selektor", image: "/mariohalas.png" }
];
</script>

<template>
  <!-- Header Section -->
  <header class="w-full relative bg-blue-800 text-white min-h-[600px] flex items-center font-lato">
    <div class="container mx-auto flex flex-col md:flex-row items-center justify-between px-8 pt-20">
      <!-- Left Side: Club Info and Buttons -->s
      <div class="md:w-1/2 text-center md:text-left">
        <h1 class="text-4xl md:text-5xl font-bold leading-tight">
          Dobrodošli u FK Janošik
        </h1>
        <p class="text-lg mt-4 mb-8">
          Klub sa tradicijom, strašću i snagom tima koji se bori do poslednjeg trenutka!
        </p>
        <a href="#" class="bg-yellow-500 text-white px-6 py-3 rounded-md font-semibold hover:bg-yellow-600">
          Pogledajte raspored
        </a>
        <a href="#" class="text-white px-6 py-3 rounded-md font-semibold ml-4">
          Saznaj više
        </a>
      </div>
      <!-- Image Placeholder -->
      <div class="md:w-1/2 flex justify-center md:justify-end mt-8 md:mt-0">
        <img src="/public/fkjanosik-logo.png" alt="FK Janosik Tim" class="w-1/2 rounded-lg shadow-lg">
      </div>
    </div>
  </header>

  <!-- Players Section -->
  <section class="container mx-auto px-8 py-12">
    <h2 class="text-3xl font-bold text-center mb-8">Naši Igrači</h2>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-8">
      <!-- Example Player Card -->
      <div v-for="(player, index) in players" :key="index" class="bg-white p-6 rounded-lg shadow-md text-center">
        <img :src="player.image" :alt="`Slika igrača ${player.name}`" class="w-full object-cover mb-4 rounded-md">
        <h3 class="text-xl font-semibold">{{ player.name }}</h3>
        <p class="text-gray-600">Godine: {{ player.age }}</p>
        <p class="text-gray-600">Pozicija: {{ player.position }}</p>
      </div>
    </div>
  </section>

  <!-- About Club Section -->
  <section class="bg-gray-100 py-12">
    <div class="container mx-auto px-8 text-center">
      <h2 class="text-3xl font-bold mb-6">O Klubu</h2>
      <p class="text-lg text-gray-700 leading-relaxed">
        FK Janosik je fudbalski klub sa bogatom istorijom i posvećenim članovima. Naša misija je da promovišemo sport, timski rad i posvećenost među mladima i starijima, a naši rezultati su dokaz posvećenosti kluba.
      </p>
    </div>
  </section>
</template>
