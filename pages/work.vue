<template>
  <DefaultLayoutVue>
    <main>
      <div class="py-10 sm:py-12">
        <div class="mx-auto max-w-7xl px-6 text-center lg:px-8">
          <div class="mx-auto max-w-2xl">
            <h2 class="text-3xl font-bold tracking-tight text-white sm:text-4xl">My Featured Work</h2>
            <p class="mt-4 text-lg leading-8 text-gray-400">
              Here is a collection of my featured work for my portfolio.
            </p>
            <p class="mt-2 text-md leading-8 text-gray-400">
              <a href="https://github.com/Matthewenderle/" target="_blank"
                >See more on my GitHub <span aria-hidden="true">→</span></a
              >
            </p>
          </div>
          <ul
            role="list"
            class="mx-auto mt-20 grid grid-cols-1 gap-6 sm:grid-cols-2 lg:grid-cols-3 lg:gap-8"
            style="max-width: none"
          >
            <li v-for="item in work" :key="item.name" class="rounded-2xl bg-zinc-900 px-8 py-10 min-w-[300px]">
              <img v-if="item.imageUrl" class="mx-auto h-48 rounded-md md:h-56" :src="item.imageUrl" alt="" />
              <h3 class="mt-6 text-base font-semibold leading-7 tracking-tight text-white">
                <a :href="item.href" target="_blank">{{ item.name }}</a>
              </h3>
              <p class="text-sm leading-6 text-gray-400">{{ item.description }}</p>
              <ul role="list" class="mt-6 flex justify-center gap-x-1">
                <li v-for="badge in item.badges" :key="badge">
                  <img class="h-6" aria-hidden="true" :src="badge" />
                </li>
              </ul>
            </li>
          </ul>
        </div>
      </div>
    </main>
  </DefaultLayoutVue>
</template>

<script setup>
import DefaultLayoutVue from '~/layouts/DefaultLayout.vue';

const work = [
  {
    name: 'EmbroideryNerd.io',
    description: 'Fullstack SaaS',
    imageUrl: '/imgs/work/embroiderynerd-io.png',
    href: 'https://embroiderynerd.io/',
    badges: [
      'https://camo.githubusercontent.com/93136bc5370d16c4008986a990bb8c5c65da020248b8a1fcabc8e8fbd3ff9523/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f6e757874332d3644413535463f7374796c653d666f722d7468652d6261646765266c6f676f3d6e757874646f746a73266c6f676f436f6c6f723d7768697465',
      'https://camo.githubusercontent.com/19ca7081b2deae02a5319753808efb3c48504ddee2f64224aae6eb7449b4c97a/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f73757061626173652d2532333430346435392e7376673f7374796c653d666f722d7468652d6261646765266c6f676f3d7375706162617365',
      'https://camo.githubusercontent.com/dab79babb38be5aada7c6f056604e2fc2ce75d82a0906676badcb34d372fd4ea/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f7461696c77696e642d3138363743303f7374796c653d666f722d7468652d6261646765266c6f676f3d7461696c77696e64637373',
      'https://camo.githubusercontent.com/924c176bc878cfe92e20a149383d2407a0244cbc10fc7c733185c7c351c46ef6/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f7374726970652d3138363743303f7374796c653d666f722d7468652d6261646765266c6f676f3d737472697065',
      'https://camo.githubusercontent.com/d90c259fd6d75363192a8e5f3a954aee6d51ddc4b3d7200afb93c187cce72bda/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f6469676974616c6f6365616e2d3138363743303f7374796c653d666f722d7468652d6261646765266c6f676f3d6469676974616c6f6365616e',
    ],
  },
  {
    name: 'Embroidery Thread Palette Converter',
    description: 'Python based Adobe/CorelDraw Palette Converter',
    imageUrl: '/imgs/work/embroiderythreadpaletteconverter.png',
    href: 'https://github.com/Matthewenderle/Embroidery-Thread-Palette-Converter',
    badges: [
      'https://camo.githubusercontent.com/0562f16a4ae7e35dae6087bf8b7805fb7e664a9e7e20ae6d163d94e56b94f32d/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f707974686f6e2d3336373041303f7374796c653d666f722d7468652d6261646765266c6f676f3d707974686f6e266c6f676f436f6c6f723d666664643534',
    ],
  },
  {
    name: 'Stop-motion Embroidery Design Parser',
    description: 'A Python script to turn any DST file into a stop-motion enabled design',
    imageUrl: '/imgs/work/stopmotionembroidery.gif',
    href: 'https://github.com/Matthewenderle/Stop-motion-Embroidery-Design-Parser',
    badges: [
      'https://camo.githubusercontent.com/0562f16a4ae7e35dae6087bf8b7805fb7e664a9e7e20ae6d163d94e56b94f32d/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f707974686f6e2d3336373041303f7374796c653d666f722d7468652d6261646765266c6f676f3d707974686f6e266c6f676f436f6c6f723d666664643534',
    ],
  },
  {
    name: 'EMF to SVG Watchdog',
    description:
      'A Python script to monitor a folder, convert EMF files to SVG using Inkscape, and move them to another folder.',
    imageUrl: null,
    href: 'https://github.com/Matthewenderle/EMF-to-SVG-Watchdog',
    badges: [
      'https://camo.githubusercontent.com/0562f16a4ae7e35dae6087bf8b7805fb7e664a9e7e20ae6d163d94e56b94f32d/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f707974686f6e2d3336373041303f7374796c653d666f722d7468652d6261646765266c6f676f3d707974686f6e266c6f676f436f6c6f723d666664643534',
    ],
  },
];
</script>
