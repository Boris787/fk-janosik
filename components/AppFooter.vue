<script setup lang="ts"></script>

<template>
    <footer class="w-full bg-gray-900 text-gray-100 py-16">
        <div class="container mx-auto px-8">
            <!-- Top Section: Club Logo and Info -->
            <div class="flex flex-col md:flex-row justify-between items-center text-center md:text-left mb-12">
                <!-- Logo and Club Info -->
                <div class="flex flex-col items-center md:items-start mb-6 md:mb-0">
                    <img src="/public/fkjanosik-logo.png" alt="Club Logo" class="w-20 h-20 mb-4">
                    <h4 class="text-xl font-semibold">Fk Janošik</h4>
                    <p class="text-gray-400 text-sm mt-2">Ponosni i strastveni od 1937</p>
                </div>

                <!-- Contact Information -->
                <div class="flex flex-col items-center md:items-end">
                    <h5 class="text-lg font-semibold">Pozovite Nas</h5>
                    <p class="text-gray-400">Email: fkjanosik@gmail.com</p>
                    <p class="text-gray-400">Phone: +381 0621946986</p>
                </div>
            </div>

            <!-- Middle Section: Links and Social Media -->
            <div class="grid grid-cols-2 md:grid-cols-4 gap-8 text-center md:text-left mb-12">
                <!-- Links Column 1 -->
                <div>
                    <h5 class="font-semibold text-lg mb-4">Klub</h5>
                    <ul class="space-y-2">
                        <li><a href="#" class="hover:underline">O Nama</a></li>
                        <li><a href="#" class="hover:underline">Naša Istorija</a></li>
                        <li><a href="#" class="hover:underline">Karijera</a></li>
                    </ul>
                </div>
                <!-- Links Column 2 -->
                <div>
                    <h5 class="font-semibold text-lg mb-4">Tim</h5>
                    <ul class="space-y-2">
                        <li><a href="#" class="hover:underline">Igrači</a></li>
                        <li><a href="#" class="hover:underline">Treneri</a></li>
                        <li><a href="#" class="hover:underline">Akademija</a></li>
                    </ul>
                </div>
                <!-- Links Column 3 -->
                <div>
                    <h5 class="font-semibold text-lg mb-4">Utakmice</h5>
                    <ul class="space-y-2">
                        <li><a href="#" class="hover:underline">Zakazane</a></li>
                        <li><a href="#" class="hover:underline">Rezultati</a></li>
                        <li><a href="#" class="hover:underline">Karte</a></li>
                    </ul>
                </div>
                <!-- Links Column 4 -->
                <div>
                    <h5 class="font-semibold text-lg mb-4">Postanite Član</h5>
                    <ul class="space-y-2">
                        <li><a href="#" class="hover:underline">Fan Klub</a></li>
                        <li><a href="#" class="hover:underline">Fk Janošik Mearch</a></li>
                        <li><a href="#" class="hover:underline">Newsletter</a></li>
                    </ul>
                </div>
            </div>

            <!-- Bottom Section: Social Media Icons -->
            <div class="flex justify-center md:justify-end space-x-6">
                <a href="#" class="text-gray-400 hover:text-white">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" viewBox="0 0 24 24" fill="currentColor">
                        <path d="M22 12.09c0-5.4-4.49-9.79-10-9.79S2 6.69 2 12.09c0 4.7 3.41 8.59 7.89 9.55v-6.77H7.89V12h2.01V9.84c0-2 1.18-3.11 3-3.11.87 0 1.76.16 1.76.16v2.01h-1c-1 0-1.31.6-1.31 1.27V12h2.19l-.35 2.87H12.3v6.77c4.48-.96 7.89-4.85 7.89-9.55z"/>
                    </svg>
                </a>
                <a href="#" class="text-gray-400 hover:text-white">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" viewBox="0 0 24 24" fill="currentColor">
                        <path d="M9.24 8.19H7.5V6.5h1.74V5.08C9.24 3.31 10.45 2 12.25 2c1.06 0 1.58.08 1.85.12v2.14h-1.33c-.73 0-1.14.69-1.14 1.46V6.5h2.47l-.33 1.69H11.6v5.8h-2.36V8.19z"/>
                    </svg>
                </a>
                <a href="#" class="text-gray-400 hover:text-white">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" viewBox="0 0 24 24" fill="currentColor">
                        <path d="M20.99 13.56V15.6c0 1.2-.98 2.17-2.2 2.17H5.21c-1.21 0-2.2-.97-2.2-2.17v-8c0-1.2.98-2.17 2.2-2.17h13.58c1.21 0 2.2.97 2.2 2.17v2.03c-.7-.43-1.56-.73-2.51-.73-3.03 0-5.5 2.49-5.5 5.56s2.47 5.56 5.5 5.56c.95 0 1.81-.29 2.51-.73z"/>
                    </svg>
                </a>
            </div>
        </div>
    </footer>
</template>
