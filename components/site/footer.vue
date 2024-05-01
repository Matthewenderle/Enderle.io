<template>
  <footer class="bg-zinc-800 border border-x-0 border-b-0 border-t-gray-600" aria-labelledby="footer-heading">
    <h2 id="footer-heading" class="sr-only">Footer</h2>
    <div class="mx-auto max-w-7xl px-6 pb-8 pt-16 sm:pt-24 lg:px-8 lg:pt-32">
      <div class="xl:grid xl:grid-cols-3 xl:gap-8">
        <div class="space-y-8">
          <img class="h-7" src="/favicon-32x32.png" alt="Enderle.io" />
          <p class="text-sm leading-6 text-gray-300">"Ensuring bad things happen to bad bugs"</p>
          <div class="flex space-x-6">
            <div class="flex justify-center space-x-6 md:order-2">
              <NuxtLink
                v-for="item in socialMedia"
                :key="item.name"
                :to="item.href"
                as="a"
                class="text-gray-400 hover:text-gray-500"
              >
                <span class="sr-only">{{ item.name }}</span>
                <icon :name="item.icon" class="h-6 w-6" aria-hidden="true" />
              </NuxtLink>
            </div>
          </div>
        </div>
        <div class="mt-16 grid grid-cols-2 gap-8 xl:col-span-2 xl:mt-0">
          <div class="md:grid md:grid-cols-2 md:gap-8">
            <div>
              <h3 class="text-sm font-semibold leading-6 text-white">Site Links</h3>
              <ul role="list" class="mt-6 space-y-4">
                <li v-for="item in navigation.site" :key="item.name">
                  <a :href="item.href" class="text-sm leading-6 text-gray-300 hover:text-white">{{ item.name }}</a>
                </li>
              </ul>
            </div>
            <div class="mt-10 md:mt-0">
              <h3 class="text-sm font-semibold leading-6 text-white">My Projects</h3>
              <ul role="list" class="mt-6 space-y-4">
                <li v-for="item in navigation.tools" :key="item.name">
                  <a :href="item.href" class="text-sm leading-6 text-gray-300 hover:text-white">{{ item.name }}</a>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
      <div class="mt-16 border-t border-white/10 pt-8 sm:mt-20 lg:mt-24">
        <p class="text-xs leading-5 text-gray-400">&copy; 2024 Enderle.io. All rights reserved.</p>
      </div>
    </div>
  </footer>
</template>

<script setup>
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

const navigation = {
  site: [
    { name: 'About', href: 'about' },
    { name: 'Work', href: 'work' },
    // { name: 'Resume', href: 'resume' },
    // { name: 'Contact', href: 'contact' },
  ],
  tools: [
    { name: 'EmbroideryNerd.io', href: 'https://embroiderynerd.io' },
    {
      name: 'Embroidery Thread Palettes',
      href: 'https://github.com/Matthewenderle/Embroidery-Thread-Palette-Converter',
    },
  ],
};
</script>
