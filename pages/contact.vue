<template>
  <DefaultLayoutVue>
    <main>
      <div class="py-16 sm:py-32">
        <div class="mx-auto max-w-7xl px-6 lg:px-8">
          <div class="mx-auto max-w-2xl space-y-16 divide-y divide-gray-100 lg:mx-0 lg:max-w-none">
            <div class="grid grid-cols-1 gap-x-8 gap-y-10 lg:grid-cols-3">
              <div>
                <h2 class="text-3xl font-bold tracking-tight text-white">Need to reach out?</h2>
                <p class="mt-4 leading-7 text-gray-300">Contact me using any of my links listed.</p>
              </div>
              <div class="grid grid-cols-1 gap-6 sm:grid-cols-2 lg:col-span-2 lg:gap-8">
                <div class="rounded-2xl bg-zinc-700 p-10">
                  <h3 class="text-base font-semibold leading-7 text-white">Email</h3>
                  <dl class="mt-3 space-y-1 text-sm leading-6 text-gray-300">
                    <div>
                      <dt class="sr-only">Email</dt>
                      <dd>
                        <a class="font-semibold text-sky-300" href="mailto:matt@enderle.io">matt@enderle.io</a>
                      </dd>
                    </div>
                  </dl>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </main>
  </DefaultLayoutVue>
</template>

<script setup>
import DefaultLayoutVue from '~/layouts/DefaultLayout.vue';
</script>
