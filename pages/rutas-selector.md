---
layout: section
routeAlias: rutas
background: https://images.unsplash.com/photo-1555066931-4365d14bab8c?auto=format&fit=crop&w=1920&q=40
---

<div class="text-teal-300 text-sm tracking-widest uppercase font-semibold mb-2">Planes de Carrera</div>

# Rutas de Aprendizaje

<div class="text-gray-200 mt-2">Elige la especialización que quieres explorar</div>

---
transition: slide-up
layout: center
---

# ¿Qué especialista quieres ser?

<div class="grid grid-cols-3 gap-4 mt-6 max-w-5xl mx-auto">

<button @click="$slidev.nav.go('ruta-bd')" class="p-5 rounded-2xl border-2 border-teal-300 bg-teal-50 hover:bg-teal-100 hover:scale-105 transition-all cursor-pointer text-center shadow-sm">
  <div class="text-4xl mb-2">🗄️</div>
  <div class="text-teal-700 font-bold text-base">Bases de Datos</div>
  <div class="text-xs text-gray-500 mt-1">SQL · Modelado · Big Data</div>
</button>

<button @click="$slidev.nav.go('ruta-backend')" class="p-5 rounded-2xl border-2 border-blue-300 bg-blue-50 hover:bg-blue-100 hover:scale-105 transition-all cursor-pointer text-center shadow-sm">
  <div class="text-4xl mb-2">⚙️</div>
  <div class="text-blue-700 font-bold text-base">Backend</div>
  <div class="text-xs text-gray-500 mt-1">APIs · Microservicios · Cloud</div>
</button>

<button @click="$slidev.nav.go('ruta-frontend')" class="p-5 rounded-2xl border-2 border-pink-300 bg-pink-50 hover:bg-pink-100 hover:scale-105 transition-all cursor-pointer text-center shadow-sm">
  <div class="text-4xl mb-2">🎨</div>
  <div class="text-pink-700 font-bold text-base">Frontend</div>
  <div class="text-xs text-gray-500 mt-1">HTML · CSS · React · UI/UX</div>
</button>

<button @click="$slidev.nav.go('ruta-ciberseguridad')" class="p-5 rounded-2xl border-2 border-red-300 bg-red-50 hover:bg-red-100 hover:scale-105 transition-all cursor-pointer text-center shadow-sm">
  <div class="text-4xl mb-2">🛡️</div>
  <div class="text-red-700 font-bold text-base">Ciberseguridad</div>
  <div class="text-xs text-gray-500 mt-1">Redes · Pentesting · Defensa</div>
</button>

<button @click="$slidev.nav.go('ruta-qa')" class="p-5 rounded-2xl border-2 border-amber-300 bg-amber-50 hover:bg-amber-100 hover:scale-105 transition-all cursor-pointer text-center shadow-sm">
  <div class="text-4xl mb-2">🧪</div>
  <div class="text-amber-700 font-bold text-base">QA & Testing</div>
  <div class="text-xs text-gray-500 mt-1">Manual · Automatización · CI</div>
</button>

</div>

<div class="mt-8 text-center">
  <button @click="$slidev.nav.go(1)" class="px-5 py-2 rounded-full border border-gray-300 bg-gray-100 text-gray-600 text-sm font-medium hover:bg-gray-200 transition-colors cursor-pointer">
    🏠 Volver al Inicio
  </button>
</div>
