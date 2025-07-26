<script setup>
import { ref } from 'vue'
// import OurSolutionImage from '@/../public/OurSolutionImage.webp'
// import DPrizeImage from '@/../public/DPrizeImage.webp'
import HeroImage from '@/../public/heroImage.webp'
// import TestimonialImage from '@/../public/TestimonialImage.webp'
// import QuotationIcon from '@/../public/QuotationIcon.webp'

const isMobileMenuOpen = ref(false)

const toggleMobileMenu = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value
}
</script>
<template>
  <header class="flex justify-between items-center px-4 md:px-8 py-4 text-black relative">
    <div class="text-xl font-bold">CLEARSIGHT</div>

    <!-- Desktop Navigation -->
    <nav class="hidden md:flex space-x-8">
      <a href="#" class="pointer-cursor hover:text-accentGold">Home</a>
      <a href="#" class="pointer-cursor hover:text-accentGold">About</a>
      <a href="#" class="pointer-cursor hover:text-accentGold">Our Work</a>
      <a href="#" class="pointer-cursor hover:text-accentGold">Impact</a>
      <a href="#" class="pointer-cursor hover:text-accentGold">Get Involved</a>
    </nav>

    <!-- Desktop Buttons -->
    <div class="hidden md:flex space-x-4">
      <button class="px-4 py-2 bg-blue-700 pointer-cursor hover:bg-accentBlue text-white rounded">
        Get Involved
      </button>
      <button class="px-4 py-2 bg-accentGold pointer-cursor hover:bg-yellow-500 text-white rounded">
        Donate
      </button>
    </div>

    <!-- Mobile Menu Button -->
    <button
      @click="toggleMobileMenu"
      class="md:hidden flex flex-col space-y-1 p-2"
      aria-label="Toggle mobile menu"
    >
      <span
        class="w-6 h-0.5 bg-black transition-all duration-300"
        :class="isMobileMenuOpen ? 'rotate-45 translate-y-2' : ''"
      ></span>
      <span
        class="w-6 h-0.5 bg-black transition-all duration-300"
        :class="isMobileMenuOpen ? 'opacity-0' : ''"
      ></span>
      <span
        class="w-6 h-0.5 bg-black transition-all duration-300"
        :class="isMobileMenuOpen ? '-rotate-45 -translate-y-2' : ''"
      ></span>
    </button>

    <!-- Mobile Sliding Menu -->
    <div
      class="fixed top-0 right-0 h-full w-80 bg-white shadow-lg transform transition-transform duration-300 ease-in-out z-50 md:hidden"
      :class="isMobileMenuOpen ? 'translate-x-0' : 'translate-x-full'"
    >
      <div class="flex justify-between items-center p-4 border-b">
        <div class="text-xl font-bold">CLEARSIGHT</div>
        <button @click="toggleMobileMenu" class="p-2">
          <span class="w-6 h-0.5 bg-black block rotate-45 translate-y-1"></span>
          <span class="w-6 h-0.5 bg-black block -rotate-45 -translate-y-1"></span>
        </button>
      </div>

      <nav class="flex flex-col p-4 space-y-6">
        <a
          href="#"
          class="text-lg hover:text-accentGold transition-colors"
          @click="toggleMobileMenu"
          >Home</a
        >
        <a
          href="#"
          class="text-lg hover:text-accentGold transition-colors"
          @click="toggleMobileMenu"
          >About</a
        >
        <a
          href="#"
          class="text-lg hover:text-accentGold transition-colors"
          @click="toggleMobileMenu"
          >Our Work</a
        >
        <a
          href="#"
          class="text-lg hover:text-accentGold transition-colors"
          @click="toggleMobileMenu"
          >Impact</a
        >
        <a
          href="#"
          class="text-lg hover:text-accentGold transition-colors"
          @click="toggleMobileMenu"
          >Get Involved</a
        >
      </nav>

      <div class="flex flex-col space-y-4 p-4 mt-6">
        <button
          class="px-4 py-3 bg-blue-700 hover:bg-accentBlue text-white rounded transition-colors"
        >
          Get Involved
        </button>
        <button
          class="px-4 py-3 bg-accentGold hover:bg-yellow-500 text-white rounded transition-colors"
        >
          Donate
        </button>
      </div>
    </div>

    <!-- Mobile Menu Overlay -->
    <div
      v-if="isMobileMenuOpen"
      class="fixed inset-0 bg-black bg-opacity-50 z-40 md:hidden"
      @click="toggleMobileMenu"
    ></div>
  </header>

  <div
    class="w-full h-[500px] md:h-[700px] text-white flex flex-col justify-center bg-cover bg-center px-4 md:px-0"
    :style="`background-image: url('${HeroImage}')`"
  >
    <div class="text-4xl md:text-8xl ml-4 md:ml-28 font-bold">
      <h1>Restoring Sight.</h1>
      <h1>Restoring</h1>
      <h1>Livelihoods.</h1>
    </div>
    <p class="max-w-2xl text-base md:text-lg ml-4 md:ml-28 mt-4">
      ClearSight Initiative provides affordable reading glasses to underserved communities across
      Ethiopia empowering people to see clearly, work confidently, and live independently.
    </p>
    <button
      class="px-6 md:px-8 w-fit py-2 ml-4 md:ml-28 mt-6 md:mt-10 bg-accentGold pointer-cursor hover:bg-yellow-500 text-white rounded"
    >
      Donate
    </button>
  </div>

  <div class="bg-[#F1F5F9] py-8 md:py-10 px-4">
    <div
      class="flex flex-col md:flex-row justify-around mx-auto max-w-5xl items-center py-6 text-center space-y-6 md:space-y-0"
    >
      <div>
        <p class="text-3xl md:text-5xl font-bold text-accentBlue">1,000+</p>
        <p class="text-base md:text-lg text-gray-600">Glasses Distributed</p>
      </div>
      <div>
        <p class="text-3xl md:text-5xl font-bold text-accentBlue">5</p>
        <p class="text-base md:text-lg text-gray-600">Regions Reached</p>
      </div>
      <div>
        <p class="text-3xl md:text-5xl font-bold text-accentBlue">200+</p>
        <p class="text-base md:text-lg text-gray-600">Health Workers Trained</p>
      </div>
      <div>
        <p class="text-3xl md:text-5xl font-bold text-accentBlue">Countless</p>
        <p class="text-base md:text-lg text-gray-600">Lives Changed</p>
      </div>
    </div>
  </div>

  <!-- Why Vision Matters Section -->
  <div class="py-8 md:py-16 px-4 md:px-8">
    <div class="max-w-6xl mx-auto flex flex-col md:flex-row items-center gap-6 md:gap-12">
      <div class="flex-1 order-2 md:order-1">
        <div class="border-l-4 border-yellow-500 pl-4 mb-6">
          <h2 class="text-2xl md:text-4xl font-bold text-accentBlue">Why Vision Matters</h2>
          <p class="text-blue-600 text-base md:text-lg mt-2">Clear vision is a basic need.</p>
        </div>
        <p class="text-gray-700 text-base md:text-lg leading-relaxed">
          Over 1 billion people globally suffer from poor vision caused by presbyopia, a condition
          easily corrected with reading glasses. In Ethiopia, this simple solution remains out of
          reach for millions.
        </p>
      </div>
      <div class="flex-1 order-1 md:order-2">
        <img
          src="/public/heroImage.webp"
          alt="Person with glasses reading"
          class="w-full rounded-lg shadow-lg"
        />
      </div>
    </div>
  </div>

  <!-- Our Solution Section -->
  <div class="py-8 md:py-16 px-4 md:px-8 bg-gray-50">
    <div class="max-w-6xl mx-auto flex flex-col md:flex-row items-center gap-6 md:gap-12">
      <div class="flex-1">
        <img
          src="/public/OurSolutionImage.webp"
          alt="Person getting glasses fitted"
          class="w-full rounded-lg shadow-lg"
        />
      </div>
      <div class="flex-1">
        <div class="border-l-4 border-yellow-500 pl-4 mb-6">
          <h2 class="text-2xl md:text-4xl font-bold text-accentBlue">Our Solution</h2>
        </div>
        <p class="text-gray-700 text-base md:text-lg leading-relaxed">
          We deliver high-quality reading glasses at ultra-low cost by training local distributors,
          partnering with health systems, and using data to maximize reach. Every pair we distribute
          restores someone's ability to read, work, and thrive.
        </p>
      </div>
    </div>
  </div>

  <!-- Backed by D-Prize Section -->
  <div class="py-8 md:py-16 px-4 md:px-8">
    <div class="max-w-6xl mx-auto flex flex-col md:flex-row items-center gap-6 md:gap-12">
      <div class="flex-1 order-2 md:order-1">
        <div class="border-l-4 border-yellow-500 pl-4 mb-6">
          <h2 class="text-2xl md:text-4xl font-bold text-accentBlue">Backed by D-Prize</h2>
        </div>
        <p class="text-gray-700 text-base md:text-lg leading-relaxed mb-8">
          ClearSight Initiative is a validated project supported by D-Prize. We're scaling up
          through trusted partnerships and community-based models to reach more people in need.
        </p>
      </div>
      <div class="flex-1 order-1 md:order-2">
        <div class="bg-gray-100 p-6 md:p-8 rounded-lg text-center">
          <img
            src="/public/DPrizeImage.webp"
            alt="D-Prize Logo"
            class="w-24 md:w-32 mx-auto mb-6"
          />
          <p class="text-gray-700 font-medium mb-2 text-sm md:text-base">
            We seed new organizations
          </p>
          <p class="text-gray-700 font-medium mb-2 text-sm md:text-base">
            distributing proven poverty solutions,
          </p>
          <p class="text-gray-700 font-medium mb-4 text-sm md:text-base">all aiming to scale.</p>
          <p class="text-blue-600 font-medium text-sm md:text-base">Are you next?</p>
        </div>
      </div>
    </div>
  </div>

  <!-- Testimonial Section -->
  <div class="py-8 md:py-16 px-4 md:px-8 bg-gray-50">
    <div class="max-w-6xl mx-auto flex flex-col md:flex-row items-center gap-6 md:gap-12">
      <div class="flex-1">
        <img
          src="/public/TestimonialImage.webp"
          alt="Man reading Bible with glasses"
          class="w-full rounded-lg shadow-lg"
        />
      </div>
      <div class="flex-1">
        <img src="/public/QuotationIcon.webp" alt="Quote" class="w-12 h-12 md:w-16 md:h-16 mb-6" />
        <blockquote class="text-lg md:text-xl text-gray-700 leading-relaxed mb-6">
          "I couldn't read the Bible for years. Now I can read every day again. These glasses
          brought back not just my sight, but a part of my life I thought was gone."
        </blockquote>
        <cite class="text-gray-600 font-medium text-sm md:text-base">
          Akalework Beyene, beneficiary in Tigray
        </cite>
      </div>
    </div>
  </div>

  <!-- Get Involved Section -->
  <div class="py-8 md:py-16 px-4 md:px-8 bg-accentBlue">
    <div class="max-w-4xl mx-auto text-center text-white">
      <div class="border-x-4 md:border-x-8 border-yellow-500 px-4 mb-6 inline-block">
        <h2 class="text-3xl md:text-5xl font-bold">Get Involved</h2>
      </div>
      <p class="text-xl md:text-3xl font-semibold mb-8">
        You can help us restore sight across Ethiopia.
      </p>
      <div class="text-base md:text-lg leading-relaxed">
        <span class="font-semibold">Donate</span> to put glasses in someone's hands,
        <span class="font-semibold">Partner</span> to expand our reach,
        <span class="font-semibold">Share our mission</span> to bring vision to all
      </div>
    </div>
  </div>

  <!-- Footer -->
  <footer class="bg-gray-100 py-8 md:py-12 px-4 md:px-8">
    <div class="max-w-6xl mx-auto">
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
        <!-- Logo and Description -->
        <div class="col-span-1 md:col-span-2 lg:col-span-1">
          <h3 class="text-xl font-bold mb-4">CLEARSIGHT LOGO</h3>
          <p class="text-gray-600 text-sm leading-relaxed">
            Restoring sight to underserved communities in Ethiopia through affordable, quality
            reading glasses.
          </p>
        </div>

        <!-- Quick Links -->
        <div>
          <h4 class="font-semibold mb-4">QUICK LINKS</h4>
          <ul class="space-y-2 text-sm text-gray-600">
            <li><a href="#" class="hover:text-accentGold">Home</a></li>
            <li><a href="#" class="hover:text-accentGold">About</a></li>
            <li><a href="#" class="hover:text-accentGold">Our Work</a></li>
            <li><a href="#" class="hover:text-accentGold">Impact</a></li>
            <li><a href="#" class="hover:text-accentGold">Get Involved</a></li>
          </ul>
        </div>

        <!-- Contact Info -->
        <div>
          <h4 class="font-semibold mb-4">CONTACT INFO</h4>
          <div class="space-y-2 text-sm text-gray-600">
            <p>Ayda Sub-city, Ethiovitian<br />Street, Mekelle, Ethiopia</p>
            <p class="text-blue-600">clearsight2017@gmail.com</p>
            <p>+251 911 037 207</p>
            <p>Social media icons</p>
          </div>
        </div>

        <!-- Newsletter -->
        <div>
          <h4 class="font-semibold mb-4">NEWSLETTER</h4>
          <div class="space-y-3">
            <button
              class="w-full py-2 px-4 border border-gray-300 rounded text-sm hover:bg-gray-50"
            >
              Partner With Us
            </button>
            <button
              class="w-full py-2 px-4 bg-accentGold text-white rounded text-sm hover:bg-yellow-500"
            >
              Donate
            </button>
          </div>
        </div>
      </div>

      <!-- Copyright -->
      <div class="border-t border-gray-300 mt-8 pt-6 text-center">
        <p class="text-sm text-gray-600">
          © Copyright 2025. All Rights Reserved by <span class="font-semibold">ClearSight</span>
        </p>
      </div>
    </div>
  </footer>
</template>
