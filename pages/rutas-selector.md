---
layout: section
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

<div class="grid grid-cols-3 gap-6 mt-8 max-w-5xl mx-auto">

<button @click="$slidev.nav.go(10)" class="p-6 rounded-2xl border-2 border-teal-300 bg-teal-50 hover:bg-teal-100 hover:scale-105 transition-all cursor-pointer text-center shadow-sm">
  <div class="text-5xl mb-3">🗄️</div>
  <div class="text-teal-700 font-bold text-lg">Bases de Datos</div>
  <div class="text-xs text-gray-500 mt-2">SQL · Modelado · Optimización · Big Data</div>
  <div class="mt-3 text-xs text-teal-600 font-medium">Ver ruta →</div>
</button>

<button @click="$slidev.nav.go(17)" class="p-6 rounded-2xl border-2 border-blue-300 bg-blue-50 hover:bg-blue-100 hover:scale-105 transition-all cursor-pointer text-center shadow-sm">
  <div class="text-5xl mb-3">⚙️</div>
  <div class="text-blue-700 font-bold text-lg">Backend</div>
  <div class="text-xs text-gray-500 mt-2">APIs · Microservicios · Seguridad · Cloud</div>
  <div class="mt-3 text-xs text-blue-600 font-medium">Ver ruta →</div>
</button>

<button @click="$slidev.nav.go(24)" class="p-6 rounded-2xl border-2 border-pink-300 bg-pink-50 hover:bg-pink-100 hover:scale-105 transition-all cursor-pointer text-center shadow-sm">
  <div class="text-5xl mb-3">🎨</div>
  <div class="text-pink-700 font-bold text-lg">Frontend</div>
  <div class="text-xs text-gray-500 mt-2">HTML · CSS · React · UI/UX</div>
  <div class="mt-3 text-xs text-pink-600 font-medium">Ver ruta →</div>
</button>

</div>

<div class="mt-8 text-center">
  <button @click="$slidev.nav.go(1)" class="px-5 py-2 rounded-full border border-gray-300 bg-gray-100 text-gray-600 text-sm font-medium hover:bg-gray-200 transition-colors cursor-pointer">
    🏠 Volver al Inicio
  </button>
</div>
