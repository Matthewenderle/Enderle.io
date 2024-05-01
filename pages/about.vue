<template>
  <DefaultLayoutVue>
    <main>
      <div class="overflow-hidden">
        <div class="relative mx-auto max-w-7xl px-6 py-16 lg:px-8">
          <div class="mx-auto text-base lg:grid lg:max-w-none lg:grid-cols-2 lg:gap-8">
            <div>
              <h2 class="text-4xl font-bold tracking-tight text-white sm:text-6xl">About Me</h2>
              <h3 class="mt-2 text-2xl font-bold leading-8 tracking-tight text-gray-300 sm:text-3xl">
                Meet Matthew Enderle
              </h3>
            </div>
          </div>
          <div class="mt-8 lg:grid lg:grid-cols-2 lg:gap-8">
            <div class="relative lg:col-start-2 lg:row-start-1">
              <div class="relative mx-auto text-base lg:max-w-none">
                <figure>
                  <div class="aspect-h-7 aspect-w-12 lg:aspect-none">
                    <img
                      class="rounded-lg object-cover object-center shadow-lg"
                      src="/imgs/matt.jpg"
                      alt="Matt in the Ocean"
                      width="1184"
                      height="1376"
                    />
                  </div>
                  <figcaption class="mt-3 flex text-sm text-gray-300">
                    <CameraIcon class="h-5 w-5 flex-none text-gray-300" aria-hidden="true" />
                    <span class="ml-2">Photograph taken at Wells-next-the-Sea, UK</span>
                  </figcaption>
                </figure>
              </div>
            </div>
            <div class="mt-8 lg:mt-0">
              <div class="mx-auto text-base lg:max-w-none">
                <p class="text-lg text-gray-300">
                  Hello! I'm Matthew L. Enderle. I'm a Web Developer specializing in Full-stack development. Experienced
                  with all stages of the development cycle for dynamic web projects. Well-versed in numerous programming
                  languages including JavaScript, SQL, PHP, and Python. I have a strong background in project management
                  and customer relations.
                </p>
              </div>
              <div class="mx-auto mt-8 text-gray-300 lg:col-start-1 lg:row-start-1 lg:max-w-none space-y-4">
                <p>
                  I originally started with website design back in 2006 when my Uncle Troy showed me Microsoft FrontPage
                  2003. I started by designing the website for our family-ran elk ranch.
                </p>
                <p>
                  Later on, I was brought onto the Lomira School District Technology team and I started writing several
                  Windows Batch scripts to automate the process for creating new accounts for students. This is where my
                  love for automation started.
                </p>
                <p>
                  After joining the U.S Air Force in 2013, I was exposed to larger systems which were significantly more
                  complicated. I had to learn how the RC-135V/W RIVET JOINT aircraft operates in order to become a
                  flying computer systems technician and operator. This also gave me the opportunity to learn how
                  multiple computer networks interact with each other, across the world, and on classified networks.
                </p>
                <p>
                  Since then, I have taken up the hobby of making Embroidered Patches. I ran into a few parts of it that
                  I hated, notably matching colors to embroidery thread/yarn was a pain. So I researched color matching
                  methods and found the CIE 2000 process and created a
                  <a href="https://github.com/Matthewenderle/RGB2Thread" target="_blank" class="text-sky-400">
                    Python GUI script</a
                  >
                  that converted the colors. Later on, I created a full fledged web app (<a
                    href="https://threadconverter.com"
                    class="text-sky-400"
                    >threadconverter.com</a
                  >) and was receiving 1-2k unique users a month.
                </p>
                <p>
                  After realizing that I had something that the public wanted, I ended up remaking the web app and
                  repackaged it as a SaaS. It uses Supabase for user authentication and the database, and users can
                  store thier results and other data that is pertinant to thier business. You can find this SaaS at
                  <a href="https://embroiderynerd.io" class="text-sky-400">EmbroideryNerd.io</a>.
                </p>
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
