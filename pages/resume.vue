<template>
  <DefaultLayoutVue>
    <main>
      <!-- Header section -->
      <div class="px-6 pt-14 lg:px-8">
        <div class="mx-auto max-w-2xl text-center">
          <h2 class="text-4xl font-bold tracking-tight text-white sm:text-6xl">My Resume</h2>
          <p class="my-6 text-lg leading-8 text-gray-300">
            I'm currently working on revising my resume. Please checkout my current one in the mean time. I've done a
            lot of work and have grown significantly since I made this previous version. Feel free to
            <NuxtLink to="/contact" class="text-sky-400">reach out</NuxtLink> to me and ask questions.
          </p>
          <p class="my-6 text-lg leading-8 text-gray-300">Thanks for your interest!</p>
          <p>
            <a href="https://enderle.io/resources/Enderle-Resume.pdf" target="_blank" class="text-sky-400 font-semibold"
              >View Resume</a
            >
          </p>
        </div>
      </div>
    </main>
  </DefaultLayoutVue>
</template>

<script setup>
import DefaultLayoutVue from '~/layouts/DefaultLayout.vue';
</script>
