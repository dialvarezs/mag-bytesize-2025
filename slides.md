---
theme: default
title: nf-core/mag v5
class: text-center
drawings:
  persist: false
transition: slide-left
mdc: true
accentColor: "#2ca597ff"
layout: cover
logo: ./images/mag_logo_mascot_only.svg
institutionalLogos:
  - ./images/logo_umag_white.svg
  - ./images/logo_catg_white.svg
---

<div class="text-center space-y-2">
  <div><img src="./images/nf-core_logo.svg" alt="nf-core" style="height: 4rem; display: inline-block;" /></div>
  <h1 class="!mb-0">mag v5.0</h1>
</div>

<div class="mt-10">

**Diego Alvarez S. | [<carbon-logo-github class="inline-block w-4 h-4 mb-0.75" /> dialvarezs](https://github.com/dialvarezs)**

<p>
  <span class="text-sm opacity-70">Universidad de Magallanes</span>
</p>

</div>

<div class="mt-12">

28.10.2025

</div>

<!--
-->

---
transition: slide-left
---

# nf-core / mag: Metagenome assembly pipeline

TODO: Diagram | Microorganisms -> Sequencing -> Assembly -> Binning -> MAGs

<!--
-->

---
transition: slide-left
---

# History & Maintainers

<div class="grid grid-cols-[30%_70%] gap-6">

<div class="flex flex-col justify-start">

## Timeline

<div class="space-y-5 text-base mt-4">

<div class="flex items-start gap-3">
<div class="text-2xl">🚀</div>
<div>
<div class="font-bold">v1.0 - Dec 2019</div>
<div class="text-sm opacity-80">By <strong>Hadrien Gourlé</strong></div>
</div>
</div>

<div class="flex items-start gap-3">
<div class="text-2xl">👥</div>
<div>
<div class="font-bold">Past maintainers</div>
<div class="text-sm opacity-80">Sabrina Krakau<br/>Maxime Borry</div>
</div>
</div>

<div class="flex items-start gap-3">
<div class="text-2xl">⚡</div>
<div>
<div class="font-bold">2024-2025</div>
<div class="text-sm opacity-80">Major updates v4 & v5</div>
</div>
</div>

</div>

</div>

<div>

## Current maintainers

<div>

<div class="grid grid-cols-3 gap-3 mt-4">

<div class="text-center">
<img src="./images/profiles/James.png" class="rounded-full w-20 h-20 mx-auto mb-1.5 object-cover" />
<div class="text-sm font-bold">James Fellows Yates</div>
<a href="https://github.com/jfy133" target="_blank" class="text-xs opacity-60 hover:opacity-100">@jfy133</a>
</div>

<div class="text-center">
<img src="./images/profiles/Jim.png" class="rounded-full w-20 h-20 mx-auto mb-1.5 object-cover" />
<div class="text-sm font-bold">Jim Downie</div>
<a href="https://github.com/prototaxites" target="_blank" class="text-xs opacity-60 hover:opacity-100">@prototaxites</a>
</div>

<div class="text-center">
<img src="./images/profiles/Daniel.png" class="rounded-full w-20 h-20 mx-auto mb-1.5 object-cover" />
<div class="text-sm font-bold">Daniel Straub</div>
<a href="https://github.com/d4straub" target="_blank" class="text-xs opacity-60 hover:opacity-100">@d4straub</a>
</div>

</div>

<div class="flex justify-center mt-3">
<div class="grid grid-cols-2 gap-3" style="width: 66.666%;">

<div class="text-center">
<img src="./images/profiles/Adam.png" class="rounded-full w-20 h-20 mx-auto mb-1.5 object-cover" />
<div class="text-sm font-bold">Adam Rosenbaum</div>
<a href="https://github.com/muabnezor" target="_blank" class="text-xs opacity-60 hover:opacity-100">@muabnezor</a>
</div>

<div class="text-center">
<img src="./images/profiles/Diego.png" class="rounded-full w-20 h-20 mx-auto mb-1.5 object-cover" />
<div class="text-sm font-bold">Diego Alvarez S.</div>
<a href="https://github.com/dialvarezs" target="_blank" class="text-xs opacity-60 hover:opacity-100">@dialvarezs</a>
</div>

</div>
</div>

</div>

<div class="mt-6 flex justify-center">
<div class="bg-gray-100 dark:bg-gray-800 rounded-lg px-4 py-2 flex items-center gap-3">
<img src="./images/profiles/other_contributors.png" class="h-15" />
<div>
<div class="text-sm font-bold">+ many other contributors</div>
<div class="text-xs opacity-60">Thank you all! 🙏</div>
</div>
</div>
</div>

</div>

</div>

<!--
-->

---
transition: slide-left
---

# What's new?

<div class="grid grid-cols-2 gap-8 mt-6">

<div class="space-y-6">

<div class="bg-gradient-to-br from-purple-50 to-pink-50 dark:from-purple-900/30 dark:to-pink-900/30 rounded-lg p-5">
<div class="flex items-center gap-3 mb-3">
<h2 class="text-xl m-0">Long read assembly</h2>
</div>
<div class="text-base">Using <strong>Flye</strong> and/or <strong>MetaMDBG</strong></div>
</div>

<div class="bg-gradient-to-br from-green-50 to-teal-50 dark:from-green-900/30 dark:to-teal-900/30 rounded-lg p-5">
<div class="flex items-center gap-3 mb-3">
<h2 class="text-xl m-0">New tools</h2>
</div>
<div class="space-y-2 text-sm">
<div><span class="font-bold text-teal-700 dark:text-teal-300">Binners:</span> CONCOCT</div>
<div><span class="font-bold text-teal-700 dark:text-teal-300">Bin QC:</span> CheckM, CheckM2</div>
<div><span class="font-bold text-teal-700 dark:text-teal-300">Viral/eukaryotic MAGs:</span> geNomad, Tiara, MetaEuk</div>
</div>
</div>

</div>

<div class="space-y-6">

<div class="bg-gradient-to-br from-blue-50 to-cyan-50 dark:from-blue-900/30 dark:to-cyan-900/30 rounded-lg p-5">
<div class="flex items-center gap-3 mb-3">
<h2 class="text-xl m-0">Updated tools / databases</h2>
</div>
<div class="text-base font-semibold">Basically everything!</div>
</div>

<div class="bg-gradient-to-br from-red-50 to-orange-50 dark:from-red-900/30 dark:to-orange-900/30 rounded-lg p-5 border-2 border-red-200 dark:border-red-700">
<div class="flex items-center gap-3 mb-3">
<h2 class="text-xl m-0">Deprecated</h2>
</div>
<div class="text-base font-bold text-red-700 dark:text-red-300">RAW read taxonomic profiling</div>
<div class="text-sm mt-2">→ Use <strong>nf-core / taxprofiler</strong> instead</div>
</div>

</div>

</div>

<!--
-->

---
layout: full
transition: slide-left
---

# Current workflow

<div class="mt--18 flex justify-center">
<img src="./images/mag_metromap_light.png" style="width: 90%" />
</div>

<!--
-->

---
transition: slide-left
---

# What's next?

<div class="bg-gradient-to-r from-teal-50 to-blue-50 dark:from-teal-900/30 dark:to-blue-900/30 rounded-xl p-6 mb-6">

## 🚀 v5.1.0 - Coming Soon!

<div class="grid grid-cols-3 gap-4 mt-4">

<div class="flex items-start gap-2">
<div class="text-2xl">📦</div>
<div>
<div class="font-bold text-sm">New binner</div>
<div class="text-sm">COMEBin</div>
</div>
</div>

<div class="flex items-start gap-2">
<div class="text-2xl">📚</div>
<div>
<div class="font-bold text-sm">Documentation</div>
<div class="text-sm">Improvements</div>
</div>
</div>

<div class="flex items-start gap-2">
<div class="text-2xl">🐛</div>
<div>
<div class="font-bold text-sm">Bug fixes</div>
</div>
</div>

</div>

</div>

## Feature Roadmap

<div class="grid grid-cols-2 gap-8 mt-6">

<div>

| Feature | Status |
|---------|:------:|
| **MetaBinner** support | 🔍 On Review |
| **Bin QC** by multiple tools | 🔍 On Review |
| **nf-test** snapshots | 📋 Planned (hackaton) |

</div>

<div>

| Feature | Status |
|---------|:------:|
| **BigMAG** compatibility | 🔨 In Progress |
| **Hostile** for contamination | 🔨 In Progress |
| **CoverM** for abundance | 📋 Planned |

</div>

</div>

<!--
-->

---
layout: center
class: text-center
---

# Thank you!

<div class="mt-12 space-y-8">

<div class="text-xl opacity-80">
Questions? Suggestions? Issues?
</div>

<div class="flex justify-center gap-12 text-lg">

<div>
<carbon-logo-github class="text-4xl mb-2" />
<div class="font-bold">GitHub</div>
<a href="https://github.com/nf-core/mag" target="_blank" class="text-teal-600 dark:text-teal-400 hover:underline">nf-core/mag</a>
</div>

<div>
<carbon-chat class="text-4xl mb-2" />
<div class="font-bold">Slack</div>
<a href="https://nfcore.slack.com/channels/mag" target="_blank" class="text-teal-600 dark:text-teal-400 hover:underline">#mag</a>
</div>

<div>
<carbon-document class="text-4xl mb-2" />
<div class="font-bold">Documentation</div>
<a href="https://nf-co.re/mag" target="_blank" class="text-teal-600 dark:text-teal-400 hover:underline">nf-co.re/mag</a>
</div>

</div>

</div>
