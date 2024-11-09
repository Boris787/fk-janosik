<script setup lang="ts">
import { ref } from 'vue';

// Definisanje openIndex sa tipom number | null
const openIndex = ref<number | null>(null);

// Pitanja i odgovori
const faqItems = [
  { question: "Kako mogu da poručim proizvod?", answer: "Jednostavno, odaberite proizvod, izaberite veličinu i kliknite na dugme 'Poručite odmah'." },
  { question: "Koje su opcije dostave?", answer: "Dostava se vrši putem kurirskih službi. Standardni rok isporuke je 7-10 radnih dana." },
  { question: "Koje metode plaćanja prihvatate?", answer: "Prihvatamo plaćanje putem kartica, PayPal-a i pouzećem." },
  { question: "Da li mogu da vratim proizvod?", answer: "Da, možete vratiti proizvod u roku od 14 dana od prijema, ako je u originalnom stanju." },
  { question: "Da li su proizvodi unikatni?", answer: "Da, svi naši proizvodi su dizajnirani specijalno za našu zajednicu." },
  { question: "Kako da znam koja je prava veličina?", answer: "Na stranici proizvoda ćete pronaći tabelu sa veličinama za pomoć." },
  { question: "Nudite li popuste?", answer: "Povremeno imamo promocije i popuste. Pratite nas za nove ponude!" },
  { question: "Šta ako ne dobijem proizvod?", answer: "U slučaju da ne dobijete proizvod, kontaktirajte nas odmah i rešićemo problem." },
  { question: "Da li šaljete izvan Srbije?", answer: "Trenutno šaljemo samo unutar Srbije, ali uskoro planiramo međunarodnu dostavu." },
  { question: "Kada će biti dostupni novi proizvodi?", answer: "Pratite naš sajt i društvene mreže za najnovije proizvode!" },
  { question: "Kako da kontaktiram korisničku podršku?", answer: "Korisnička podrška je dostupna putem email-a ili kontakt forme na sajtu." }
];

// Funkcija za toggle odgovora
const toggleAnswer = (index: number) => {
  openIndex.value = openIndex.value === index ? null : index;
};
</script>

<template>
  <!-- FAQ Section -->
  <section class="container mx-auto px-8 pb-10 pt-28">
    <h2 class="text-3xl font-bold text-center mb-8">Potražite odgovore na najčešća pitanja</h2>

    <div class="space-y-4">
      <!-- FAQ Item -->
      <div v-for="(item, index) in faqItems" :key="index" class="faq-item bg-white rounded-lg shadow-lg overflow-hidden">
        <div
          :class="['question cursor-pointer p-4', openIndex === index ? 'bg-blue-600 text-white' : 'bg-gray-100 text-gray-800']"
          @click="toggleAnswer(index)"
        >
          <h3 class="text-xl font-semibold">{{ item.question }}</h3>
        </div>
        <div v-if="openIndex === index" class="answer bg-gray-50 p-4 text-gray-700">
          <p>{{ item.answer }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.faq-item {
  transition: all 0.3s ease;
}

.question {
  transition: background-color 0.3s, color 0.3s;
}

.question:hover {
  background-color: #3182ce;
  color: white;
}

@media (max-width: 768px) {
  .faq-item {
    margin-bottom: 1rem;
  }

  .question {
    font-size: 1rem;
  }

  .answer {
    font-size: 0.9rem;
  }
}
</style>
