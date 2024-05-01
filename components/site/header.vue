<template>
  <Disclosure v-slot="{ open }" as="nav" class="bg-zinc-800 border border-x-0 border-t-0 border-b-gray-600">
    <div class="mx-auto max-w-7xl px-2 sm:px-6 lg:px-8">
      <div class="relative flex h-16 items-center justify-between">
        <div class="absolute inset-y-0 left-0 flex items-center sm:hidden">
          <!-- Mobile menu button-->
          <DisclosureButton
            class="relative inline-flex items-center justify-center rounded-md p-2 text-white hover:bg-zinc-700 hover:text-white focus:outline-none focus:ring-2 focus:ring-inset focus:ring-white"
          >
            <span class="absolute -inset-0.5" />
            <span class="sr-only">Open main menu</span>
            <icon v-if="!open" name="heroicons:bars-3" class="block h-6 w-6" aria-hidden="true" />
            <icon v-else name="heroicons:x-mark" class="block h-6 w-6" aria-hidden="true" />
          </DisclosureButton>
        </div>
        <div class="flex flex-1 items-center justify-center sm:items-stretch sm:justify-start">
          <div class="flex flex-shrink-0 items-center bg-zinc-800 border border-y-0 border-l-0 border-b-gray-600">
            <NuxtLink to="/"><span class="text-4xl mr-4 font-bold font-mono text-white">Enderle.io</span></NuxtLink>
          </div>
          <div class="hidden sm:ml-6 sm:block">
            <div class="flex space-x-4">
              <a
                v-for="item in navigation"
                :key="item.name"
                :to="item.to"
                :class="[
                  item.current ? 'bg-zinc-900 text-white' : 'text-zinc-300 hover:bg-zinc-700 hover:text-white',
                  'rounded-md px-3 py-2 text-sm font-medium',
                ]"
                :aria-current="item.current ? 'page' : undefined"
                @click="goTo(item.to)"
              >
                {{ item.name }}
              </a>
            </div>
          </div>
        </div>
        <div class="absolute inset-y-0 right-0 flex items-center pr-2 sm:static sm:inset-auto sm:ml-6 sm:pr-0"></div>
      </div>
    </div>

    <DisclosurePanel class="sm:hidden">
      <div class="space-y-1 px-2 pb-3 pt-2">
        <a v-for="item in navigation" :key="item.name" as="a" @click="goTo(item.to)">
          <DisclosureButton
            as="a"
            :to="item.to"
            :class="[
              item.current ? 'bg-zinc-900 text-white' : 'text-zinc-300 hover:bg-zinc-700 hover:text-white',
              'block rounded-md px-3 py-2 text-base font-medium',
            ]"
            :aria-current="item.current ? 'page' : undefined"
            >{{ item.name }}</DisclosureButton
          ></a
        >
      </div>
    </DisclosurePanel>
  </Disclosure>
</template>

<script setup>
import { Disclosure, DisclosureButton, DisclosurePanel } from '@headlessui/vue';

const route = useRoute();

const navigation = [
  { name: 'About', to: 'about', current: true },
  { name: 'Work', to: 'work', current: false },
  // { name: 'Resume', to: 'resume', current: false },
  // { name: 'Contact', to: 'contact', current: false },
];

const goTo = (routePath) => {
  console.log(routePath);
  if (route.path !== routePath) {
    navigateTo(routePath);
    setActiveAndOpen(navigation);
  }
};

const setActiveAndOpen = (items) => {
  items.forEach((item) => {
    const isActiveRoute = route.name === item.to || route.name.startsWith(item.to);
    item.current = isActiveRoute; // Highlight current item
    if (item.children) {
      item.children.forEach((subItem) => {
        const isSubItemActive = route.path === subItem.to;
        subItem.current = isSubItemActive;
        if (isSubItemActive) {
          item.open = true; // Automatically open parent if sub-item is active
        }
      });
    }
  });
};

onBeforeMount(async () => {
  setActiveAndOpen(navigation);
});
</script>
