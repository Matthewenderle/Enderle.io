<template>
  <DefaultLayoutVue>
    <main>
      <!-- Header section -->
      <div class="mx-auto max-w-7xl px-6 pb-24 sm:pb-32 lg:flex lg:px-8 lg:py-40 py-16 align-middle">
        <div id="headerContent" class="px-6 lg:px-8">
          <div class="mx-auto max-w-2xl text-center sm:pt-20">
            <h2 class="text-4xl font-bold tracking-tight text-white sm:text-6xl">Freelance Full-stack Developer</h2>
            <p class="mt-6 text-lg leading-8 text-gray-300">
              Matthew specializes in Full-stack web development. He spends his time researching ways to automate
              processes and increase effeciencies.
            </p>
            <div class="flex mt-6 justify-center space-x-6 md:order-2">
              <a
                v-for="item in socialMedia"
                :key="item.name"
                :href="item.href"
                class="text-gray-400 hover:text-gray-500"
              >
                <span class="sr-only">{{ item.name }}</span>
                <icon :name="item.icon" class="h-6 w-6" aria-hidden="true" />
              </a>
            </div>
            <div class="mt-10 flex items-center gap-x-6">
              <NuxtLink
                to="/about"
                class="rounded-md bg-zinc-500 px-3.5 py-2.5 text-sm font-semibold text-white shadow-sm hover:bg-zinc-400 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-zinc-400"
                >About Me</NuxtLink
              >
              <NuxtLink to="/work" class="text-sm font-semibold leading-6 text-white"
                >See my work <span aria-hidden="true">→</span></NuxtLink
              >
            </div>
          </div>
        </div>

        <div
          id="headerImage"
          class="mx-auto mt-16 flex max-w-2xl sm:mt-24 lg:ml-10 lg:mr-0 lg:mt-0 lg:max-w-none lg:flex-none xl:ml-32"
        >
          <div class="max-w-3xl md:flex-none sm:max-w-5xl lg:max-w-none">
            <img
              src="/imgs/mattWithCamera.jpg"
              alt="App screenshot"
              class="w-[60rem] rounded-md bg-white/5 shadow-2xl ring-1 ring-white/10"
            />
          </div>
        </div>
      </div>

      <ContentDoc v-if="false" />
    </main>
  </DefaultLayoutVue>
</template>

<script setup>
import DefaultLayoutVue from '~/layouts/DefaultLayout.vue';

const socialMedia = [
  {
    name: 'Facebook',
    href: 'https://www.facebook.com/menderle/',
    icon: 'fa6-brands:facebook',
  },
  {
    name: 'Instagram',
    href: 'https://www.instagram.com/matthewenderle/',
    icon: 'fa6-brands:instagram',
  },
  {
    name: 'Github',
    href: 'https://github.com/Matthewenderle',
    icon: 'fa6-brands:github',
  },
  {
    name: 'Twitter',
    href: 'https://twitter.com/MatthewEnderle',
    icon: 'fa6-brands:twitter',
  },
  {
    name: 'Flickr',
    href: 'https://www.flickr.com/photos/128435984@N08/',
    icon: 'fa6-brands:flickr',
  },
  {
    name: 'LinkedIn',
    href: 'https://www.linkedin.com/in/matthew-enderle-116b6370/',
    icon: 'fa6-brands:linkedin',
  },
];
</script>
