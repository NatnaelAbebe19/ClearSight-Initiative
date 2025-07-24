<script setup>
import OurSolutionImage from '/public/ourSolutionImage.webp'
import DPrizeImage from '/public/dPrizeImage.webp'
import HeroImage from '/public/heroImage.webp'
import TestimonialImage from '/public/testimonialImage.webp'
import QuotationIcon from '/public/quotationIcon.webp'
</script>
<template>
  <header class="flex justify-between items-center px-8 py-4 text-black">
    <div class="text-xl font-bold">CLEARSIGHT</div>
    <nav class="flex space-x-8">
      <a href="#" class="pointor-cursor hover:text-accentGold">Home</a>
      <a href="#" class="pointor-cursor hover:text-accentGold">About</a>
      <a href="#" class="pointor-cursor hover:text-accentGold">Our Work</a>
      <a href="#" class="pointor-cursor hover:text-accentGold">Impact</a>
      <a href="#" class="pointor-cursor hover:text-accentGold">Get Involved</a>
    </nav>
    <div class="flex space-x-4">
      <button class="px-4 py-2 bg-blue-700 pointor-cursor hover:bg-accentBlue text-white rounded">
        Get Involved
      </button>
      <button class="px-4 py-2 bg-accentGold pointor-cursor hover:bg-yellow-500 text-white rounded">
        Donate
      </button>
    </div>
  </header>
  <div
    class="w-full h-[700px] text-white flex-col bg-cover bg-center"
    style="background-image: url('/heroImage.webp')"
  >
    <div class="text-8xl ml-28 font-bold pt-22">
      <h1 class="">Restoring Sight.</h1>
      <h1 class="">Restoring</h1>
      <h1 class="">Livelihoods.</h1>
    </div>
    <p class="max-w-2xl text-lg ml-28 mt-4">
      ClearSight Initiative provides affordable reading glasses to underserved communities across
      Ethiopia empowering people to see clearly, work confidently, and live independently.
    </p>
    <button
      class="px-8 round-md w-fit py-2 ml-28 mt-10 bg-accentGold pointor-cursor hover:bg-yellow-500 text-white rounded"
    >
      Donate
    </button>
  </div>

  <div class="bg-[#F1F5F9] py-10">
    <div class="flex justify-around mx-auto max-w-5xl items-center py-6 text-center">
      <div>
        <p class="text-5xl font-bold text-accentBlue">1,000+</p>
        <p class="text-lg text-gray-600">Glasses Distributed</p>
      </div>
      <div>
        <p class="text-5xl font-bold text-accentBlue">5</p>
        <p class="text-lg text-gray-600">Regions Reached</p>
      </div>
      <div>
        <p class="text-5xl font-bold text-accentBlue">200+</p>
        <p class="text-lg text-gray-600">Health Workers Trained</p>
      </div>
      <div>
        <p class="text-5xl font-bold text-accentBlue">Countless</p>
        <p class="text-lg text-gray-600">Lives Changed</p>
      </div>
    </div>
  </div>

  <!-- Why Vision Matters Section -->
  <div class="py-16 px-8">
    <div class="max-w-6xl mx-auto flex items-center gap-12">
      <div class="flex-1">
        <div class="border-l-4 border-yellow-500 pl-4 mb-6">
          <h2 class="text-4xl font-bold text-accentBlue">Why Vision Matters</h2>
          <p class="text-blue-600 text-lg mt-2">Clear vision is a basic need.</p>
        </div>
        <p class="text-gray-700 text-lg leading-relaxed">
          Over 1 billion people globally suffer from poor vision caused by presbyopia, a condition
          easily corrected with reading glasses. In Ethiopia, this simple solution remains out of
          reach for millions.
        </p>
      </div>
      <div class="flex-1">
        <img
          :src="HeroImage"
          alt="Person with glasses reading"
          class="w-full rounded-lg shadow-lg"
        />
      </div>
    </div>
  </div>

  <!-- Our Solution Section -->
  <div class="py-16 px-8 bg-gray-50">
    <div class="max-w-6xl mx-auto flex items-center gap-12">
      <div class="flex-1">
        <img
          :src="OurSolutionImage"
          alt="Person getting glasses fitted"
          class="w-full rounded-lg shadow-lg"
        />
      </div>
      <div class="flex-1">
        <div class="border-l-4 border-yellow-500 pl-4 mb-6">
          <h2 class="text-4xl font-bold text-accentBlue">Our Solution</h2>
        </div>
        <p class="text-gray-700 text-lg leading-relaxed">
          We deliver high-quality reading glasses at ultra-low cost by training local distributors,
          partnering with health systems, and using data to maximize reach. Every pair we distribute
          restores someone's ability to read, work, and thrive.
        </p>
      </div>
    </div>
  </div>

  <!-- Backed by D-Prize Section -->
  <div class="py-16 px-8">
    <div class="max-w-6xl mx-auto flex items-center gap-12">
      <div class="flex-1">
        <div class="border-l-4 border-yellow-500 pl-4 mb-6">
          <h2 class="text-4xl font-bold text-accentBlue">Backed by D-Prize</h2>
        </div>
        <p class="text-gray-700 text-lg leading-relaxed mb-8">
          ClearSight Initiative is a validated project supported by D-Prize. We're scaling up
          through trusted partnerships and community-based models to reach more people in need.
        </p>
      </div>
      <div class="flex-1">
        <div class="bg-gray-100 p-8 rounded-lg text-center">
          <img :src="DPrizeImage" alt="D-Prize Logo" class="w-32 mx-auto mb-6" />
          <p class="text-gray-700 font-medium mb-2">We seed new organizations</p>
          <p class="text-gray-700 font-medium mb-2">distributing proven poverty solutions,</p>
          <p class="text-gray-700 font-medium mb-4">all aiming to scale.</p>
          <p class="text-blue-600 font-medium">Are you next?</p>
        </div>
      </div>
    </div>
  </div>

  <!-- Testimonial Section -->
  <div class="py-16 px-8 bg-gray-50">
    <div class="max-w-6xl mx-auto flex items-center gap-12">
      <div class="flex-1">
        <img
          :src="TestimonialImage"
          alt="Man reading Bible with glasses"
          class="w-full rounded-lg shadow-lg"
        />
      </div>
      <div class="flex-1">
        <img :src="QuotationIcon" alt="Quote" class="w-16 h-16 mb-6" />
        <blockquote class="text-xl text-gray-700 leading-relaxed mb-6">
          "I couldn't read the Bible for years. Now I can read every day again. These glasses
          brought back not just my sight, but a part of my life I thought was gone."
        </blockquote>
        <cite class="text-gray-600 font-medium"> Akalework Beyene, beneficiary in Tigray </cite>
      </div>
    </div>
  </div>

  <!-- Get Involved Section -->
  <div class="py-16 px-8 bg-accentBlue">
    <div class="max-w-4xl mx-auto text-center text-white">
      <div class="border-x-8 border-yellow-500 px-4 mb-6 inline-block">
        <h2 class="text-5xl font-bold">Get Involved</h2>
      </div>
      <p class="text-3xl font-semibold mb-8">You can help us restore sight across Ethiopia.</p>
      <div class="text-lg leading-relaxed">
        <span class="font-semibold">Donate</span> to put glasses in someone's hands,
        <span class="font-semibold">Partner</span> to expand <br />
        our reach,
        <span class="font-semibold">Share our mission</span> to bring vision to all
      </div>
    </div>
  </div>

  <!-- Footer -->
  <footer class="bg-gray-100 py-12 px-8">
    <div class="max-w-6xl mx-auto">
      <div class="grid grid-cols-4 gap-8">
        <!-- Logo and Description -->
        <div>
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
