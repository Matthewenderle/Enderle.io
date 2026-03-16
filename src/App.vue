<template>
  <div
    class="min-h-screen text-[#d1d2d4]"
    :style="{
      background:
        'radial-gradient(circle at top, rgba(34,64,154,0.18), transparent 30%), radial-gradient(circle at 0% 35%, rgba(199,32,39,0.16), transparent 26%), #040809',
    }"
  >
    <div class="mx-auto max-w-7xl px-6 py-6 sm:px-8 lg:px-10">
      <header class="sticky top-0 z-30 mb-10 rounded-2xl border border-white/10 bg-black/30 backdrop-blur-xl">
        <div class="flex flex-col gap-4 px-5 py-4 sm:flex-row sm:items-center sm:justify-between">
          <div>
            <div class="text-lg font-semibold tracking-wide text-white">Matthew Enderle</div>
            <div class="text-sm text-[#6e6f71]">Full-stack engineer for SaaS, workflow systems, and operational tooling</div>
          </div>
          <nav class="flex flex-wrap gap-3 text-sm text-[#d1d2d4]">
            <a href="#projects" class="rounded-full border border-white/10 px-4 py-2 transition hover:border-[#f4ee20] hover:text-[#f4ee20]">Projects</a>
            <a href="#about" class="rounded-full border border-white/10 px-4 py-2 transition hover:border-[#f4ee20] hover:text-[#f4ee20]">About</a>
            <a href="#contact" class="rounded-full border border-white/10 px-4 py-2 transition hover:border-[#f4ee20] hover:text-[#f4ee20]">Contact</a>
          </nav>
        </div>
      </header>

      <main>
        <section class="grid items-center gap-10 pb-12 pt-4 lg:grid-cols-[1.15fr_0.85fr] lg:pt-8">
          <div class="max-w-3xl">
            <div class="mb-5 inline-flex items-center gap-2 rounded-full border border-[#22409a]/60 bg-[#22409a]/10 px-3 py-1 text-sm text-[#d1d2d4]">
              <span class="h-2 w-2 rounded-full bg-[#f4ee20]" />
              Available for freelance, product, and platform engineering work
            </div>

            <h1 class="max-w-4xl text-4xl font-semibold leading-[1.02] text-white sm:text-5xl lg:text-[4.5rem]">
              Building <span class="text-[#f4ee20]">useful software</span> for teams with complex workflows.
            </h1>

            <p class="mt-6 max-w-2xl text-lg leading-8 text-[#d1d2d4]">
              I design and ship vertical SaaS, internal tools, client portals, and engineering interfaces that turn messy operations into clear, reliable workflows.
            </p>

            <div class="mt-8 flex flex-wrap gap-3">
              <a href="#projects" class="rounded-2xl bg-[#c72027] px-6 py-3 text-sm font-medium text-white shadow-[0_12px_40px_rgba(199,32,39,0.25)] transition hover:-translate-y-0.5">View selected projects</a>
              <a href="#contact" class="rounded-2xl border border-[#22409a] px-6 py-3 text-sm font-medium text-[#d1d2d4] transition hover:bg-[#22409a] hover:text-white">Get in touch</a>
            </div>

            <div class="mt-8 flex flex-wrap gap-3">
              <a
                v-for="link in socialLinks"
                :key="link.name"
                :href="link.href"
                target="_blank"
                rel="noreferrer"
                class="rounded-full border border-white/10 px-4 py-2 text-sm text-[#d1d2d4] transition hover:border-[#f4ee20] hover:text-[#f4ee20]"
              >
                {{ link.name }}
              </a>
            </div>
          </div>

          <div class="rounded-[28px] border border-white/10 bg-white/[0.04] p-5 shadow-2xl backdrop-blur-xl">
            <div class="overflow-hidden rounded-[22px] border border-white/10 bg-[#070b10]">
              <img src="/imgs/mattWithCamera.jpg" alt="Matthew Enderle" class="h-[360px] w-full object-cover object-center" />
            </div>

            <div class="mt-5 grid gap-3 sm:grid-cols-2">
              <div class="rounded-[22px] border border-white/10 bg-[#070b10] p-5 sm:col-span-2">
                <div class="text-sm uppercase tracking-[0.22em] text-[#6e6f71]">Core focus</div>
                <div class="mt-3 text-2xl font-semibold text-white">Product-minded engineering</div>
                <p class="mt-3 text-sm leading-7 text-[#d1d2d4]">
                  Strongest where product clarity, data modeling, and workflow-heavy UX all need to work together.
                </p>
              </div>

              <div
                v-for="item in focusAreas"
                :key="item"
                class="rounded-[22px] border border-white/10 bg-[#070b10] px-4 py-4 text-sm leading-6 text-[#d1d2d4]"
              >
                {{ item }}
              </div>
            </div>
          </div>
        </section>

        <section class="pb-8">
          <div class="grid gap-4 md:grid-cols-3">
            <div v-for="stat in stats" :key="stat.label" class="rounded-[24px] border border-white/10 bg-white/[0.04] p-6">
              <div class="text-3xl font-semibold text-white">{{ stat.value }}</div>
              <div class="mt-2 text-sm text-[#6e6f71]">{{ stat.label }}</div>
            </div>
          </div>
        </section>

        <section id="projects" class="scroll-mt-24 py-14">
          <div class="mb-8 flex flex-col gap-4 lg:flex-row lg:items-end lg:justify-between">
            <div>
              <div class="text-sm uppercase tracking-[0.26em] text-[#6e6f71]">Selected work</div>
              <h2 class="mt-2 text-3xl font-semibold text-white sm:text-4xl">Projects that prove product and engineering depth</h2>
            </div>
            <p class="max-w-2xl text-sm leading-7 text-[#d1d2d4]">
              The strongest signal comes from real products, real workflows, and systems built for real users.
            </p>
          </div>

          <div class="grid gap-6 lg:grid-cols-[1.15fr_0.85fr]">
            <article class="rounded-[30px] border border-white/10 bg-white/[0.05] p-7 transition hover:border-[#c72027]/60 hover:bg-white/[0.06]">
              <div class="flex flex-wrap items-start justify-between gap-4">
                <div>
                  <div class="text-sm uppercase tracking-[0.22em] text-[#6e6f71]">01 · Flagship product</div>
                  <h3 class="mt-2 text-3xl font-semibold text-white">{{ featuredProject.name }}</h3>
                  <div class="mt-2 text-sm text-[#f4ee20]">{{ featuredProject.category }}</div>
                </div>
                <div class="rounded-full border border-[#22409a]/40 bg-[#22409a]/10 px-3 py-1 text-xs text-[#d1d2d4]">
                  {{ featuredProject.altName }}
                </div>
              </div>

              <p class="mt-5 max-w-3xl text-base leading-8 text-[#d1d2d4]">{{ featuredProject.summary }}</p>

              <div class="mt-6 grid gap-3 sm:grid-cols-2">
                <div
                  v-for="highlight in featuredProject.highlights"
                  :key="highlight"
                  class="rounded-2xl border border-white/10 bg-black/20 px-4 py-3 text-sm text-[#d1d2d4]"
                >
                  {{ highlight }}
                </div>
              </div>

              <div class="mt-6 flex items-center justify-between gap-3 border-t border-white/10 pt-5">
                <div>
                  <div class="text-xs uppercase tracking-[0.24em] text-[#6e6f71]">Why it matters</div>
                  <div class="mt-2 text-sm text-[#d1d2d4]">Shows product ownership, workflow design, and operational thinking.</div>
                </div>
                <a :href="featuredProject.href" target="_blank" rel="noreferrer" class="rounded-2xl bg-[#c72027] px-5 py-3 text-sm font-medium text-white transition hover:-translate-y-0.5">{{ featuredProject.cta }}</a>
              </div>
            </article>

            <div class="grid gap-6">
              <article
                v-for="(project, index) in supportingProjects"
                :key="project.name"
                class="rounded-[28px] border border-white/10 bg-white/[0.045] p-6 transition duration-300 hover:-translate-y-1 hover:border-[#c72027]/60 hover:bg-white/[0.06]"
              >
                <div class="mb-4 flex items-start justify-between gap-4">
                  <div>
                    <div class="text-sm uppercase tracking-[0.22em] text-[#6e6f71]">0{{ index + 2 }}</div>
                    <h3 class="mt-2 text-2xl font-semibold text-white">{{ project.name }}</h3>
                    <div class="mt-2 text-sm text-[#f4ee20]">{{ project.category }}</div>
                  </div>
                  <div class="rounded-full border border-[#22409a]/40 bg-[#22409a]/10 px-3 py-1 text-xs text-[#d1d2d4]">
                    {{ project.altName }}
                  </div>
                </div>

                <p class="text-sm leading-7 text-[#d1d2d4]">{{ project.summary }}</p>

                <div class="mt-5 flex flex-wrap gap-2">
                  <span
                    v-for="highlight in project.highlights"
                    :key="highlight"
                    class="rounded-full border border-white/10 bg-black/20 px-3 py-1 text-xs text-[#d1d2d4]"
                  >
                    {{ highlight }}
                  </span>
                </div>

                <div class="mt-6 flex items-center justify-between gap-3 border-t border-white/10 pt-5">
                  <div class="text-xs uppercase tracking-[0.24em] text-[#6e6f71]">Live product / demo</div>
                  <a :href="project.href" target="_blank" rel="noreferrer" class="rounded-2xl border border-[#d1d2d4]/20 px-4 py-2 text-sm font-medium text-white transition hover:border-[#f4ee20] hover:text-[#f4ee20]">{{ project.cta }}</a>
                </div>
              </article>
            </div>
          </div>
        </section>

        <section id="about" class="scroll-mt-24 py-14">
          <div class="grid gap-6 lg:grid-cols-[0.95fr_1.05fr]">
            <div class="rounded-[28px] border border-white/10 bg-white/[0.045] p-7">
              <div class="text-sm uppercase tracking-[0.26em] text-[#6e6f71]">About</div>
              <h2 class="mt-3 text-3xl font-semibold text-white">Product-minded, systems-capable, detail-obsessed.</h2>
              <p class="mt-5 text-sm leading-8 text-[#d1d2d4]">
                I build software for people who need clarity, speed, and reliability. That means designing around real-world constraints, automating repetitive work, and creating interfaces that help teams move faster with less friction.
              </p>
            </div>

            <div class="grid gap-6 sm:grid-cols-2">
              <div v-for="group in aboutGroups" :key="group.title" class="rounded-[28px] border border-white/10 bg-white/[0.045] p-7">
                <div class="text-lg font-semibold text-white">{{ group.title }}</div>
                <div class="mt-5 space-y-3">
                  <div v-for="item in group.items" :key="item" class="flex items-center gap-3 text-sm text-[#d1d2d4]">
                    <div class="h-2 w-2 rounded-full bg-[#22409a]" />
                    {{ item }}
                  </div>
                </div>
              </div>
            </div>
          </div>
        </section>

        <section id="contact" class="scroll-mt-24 py-14">
          <div class="rounded-[32px] border border-white/10 bg-gradient-to-br from-white/[0.06] to-white/[0.03] p-8 sm:p-10">
            <div class="max-w-3xl">
              <div class="text-sm uppercase tracking-[0.26em] text-[#6e6f71]">Contact</div>
              <h2 class="mt-3 text-3xl font-semibold text-white sm:text-4xl">Let’s build something useful.</h2>
              <p class="mt-4 text-base leading-8 text-[#d1d2d4]">
                Interested in product engineering, internal tools, simulation interfaces, or workflow-heavy SaaS? Reach out and I’ll be glad to connect.
              </p>
            </div>

            <div class="mt-8 flex flex-wrap gap-4">
              <a class="rounded-2xl bg-[#c72027] px-6 py-3 text-sm font-medium text-white transition hover:-translate-y-0.5" href="mailto:matthewenderle@gmail.com">matthewenderle@gmail.com</a>
              <a class="rounded-2xl border border-white/10 px-6 py-3 text-sm font-medium text-[#d1d2d4] transition hover:border-[#22409a] hover:bg-[#22409a] hover:text-white" href="https://github.com/Matthewenderle" target="_blank" rel="noreferrer">GitHub</a>
              <a class="rounded-2xl border border-white/10 px-6 py-3 text-sm font-medium text-[#d1d2d4] transition hover:border-[#f4ee20] hover:text-[#f4ee20]" href="https://www.linkedin.com/in/matthew-enderle-116b6370/" target="_blank" rel="noreferrer">LinkedIn</a>
            </div>
          </div>
        </section>
      </main>
    </div>
  </div>
</template>

<script setup>
const socialLinks = [
  { name: 'GitHub', href: 'https://github.com/Matthewenderle' },
  { name: 'LinkedIn', href: 'https://www.linkedin.com/in/matthew-enderle-116b6370/' },
  { name: 'X', href: 'https://twitter.com/MatthewEnderle' },
  { name: 'Instagram', href: 'https://www.instagram.com/matthewenderle/' },
];

const projects = [
  {
    name: 'EmbroideryNerd',
    altName: 'Potential rebrand: Bobinly',
    category: 'Flagship Vertical SaaS',
    href: 'https://embroiderynerd.io',
    summary:
      'An embroidery operations platform focused on color matching, project management, inventory tracking, and production workflow coordination.',
    highlights: [
      'Color matching workflows',
      'Project and job management',
      'Inventory tracking',
      'Operations-focused product design',
    ],
    cta: 'Visit product',
  },
  {
    name: 'Punchbase',
    altName: 'B2B SaaS',
    category: 'Client Delivery Platform',
    href: 'https://punchbase.io',
    summary:
      'A customer portal for embroidery and vector service providers that simplifies file delivery, client management, and repeatable service workflows.',
    highlights: [
      'Secure client delivery portal',
      'Service-provider workflow tooling',
      'Customer file management',
      'Production-ready B2B UX',
    ],
    cta: 'Explore platform',
  },
  {
    name: 'RadiantLink',
    altName: 'Closed-source DoD project',
    category: 'Graph Visualization System',
    href: 'https://radiantlink.enderle.io',
    summary:
      'A dynamic block and signal-flow diagram system backed by Neo4j, designed to generate interactive engineering visualizations from graph-structured data.',
    highlights: [
      'Neo4j-backed architecture',
      'Dynamic diagram generation',
      'Engineering system modeling',
      'Demo environment available',
    ],
    cta: 'View demo',
  },
  {
    name: 'LCS Emulator',
    altName: 'Closed-source DoD project',
    category: 'Training Simulation',
    href: 'https://lcsemulator.enderle.io',
    summary:
      'A liquid cooling system emulator built for training scenarios, enabling users to understand system behavior through simulation-driven interaction.',
    highlights: [
      'Training-focused simulator',
      'Interactive system behavior',
      'Domain-specific engineering UX',
      'Demo environment available',
    ],
    cta: 'Launch demo',
  },
];

const featuredProject = projects[0];
const supportingProjects = projects.slice(1);

const focusAreas = [
  'SaaS product architecture',
  'Workflow automation',
  'Operational tooling',
  'Data-driven interfaces',
];

const stats = [
  { value: '4', label: 'Featured projects' },
  { value: '2', label: 'Production SaaS products' },
  { value: '2', label: 'Closed-source engineering demos' },
];

const aboutGroups = [
  {
    title: 'What I optimize for',
    items: ['Clarity', 'Useful UX', 'Performance', 'Business value'],
  },
  {
    title: 'What I build',
    items: ['Vertical SaaS', 'B2B portals', 'Simulators', 'Data-rich interfaces'],
  },
];
</script>
