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

<div class="grid grid-cols-2 gap-5 mt-6 max-w-3xl mx-auto">

<button @click="$slidev.nav.go(10)" class="p-5 rounded-2xl border-2 border-teal-300 bg-teal-50 hover:bg-teal-100 hover:scale-105 transition-all cursor-pointer text-center shadow-sm">
  <div class="text-4xl mb-2">🗄️</div>
  <div class="text-teal-700 font-bold text-lg">Bases de Datos</div>
  <div class="text-xs text-gray-500 mt-1">SQL · Modelado · Big Data</div>
</button>

<button @click="$slidev.nav.go(17)" class="p-5 rounded-2xl border-2 border-blue-300 bg-blue-50 hover:bg-blue-100 hover:scale-105 transition-all cursor-pointer text-center shadow-sm">
  <div class="text-4xl mb-2">⚙️</div>
  <div class="text-blue-700 font-bold text-lg">Backend</div>
  <div class="text-xs text-gray-500 mt-1">APIs · Microservicios · Cloud</div>
</button>

<button @click="$slidev.nav.go(24)" class="p-5 rounded-2xl border-2 border-pink-300 bg-pink-50 hover:bg-pink-100 hover:scale-105 transition-all cursor-pointer text-center shadow-sm">
  <div class="text-4xl mb-2">🎨</div>
  <div class="text-pink-700 font-bold text-lg">Frontend</div>
  <div class="text-xs text-gray-500 mt-1">HTML · CSS · React · UI/UX</div>
</button>

<button @click="$slidev.nav.go(31)" class="p-5 rounded-2xl border-2 border-red-300 bg-red-50 hover:bg-red-100 hover:scale-105 transition-all cursor-pointer text-center shadow-sm">
  <div class="text-4xl mb-2">🛡️</div>
  <div class="text-red-700 font-bold text-lg">Ciberseguridad</div>
  <div class="text-xs text-gray-500 mt-1">Redes · Pentesting · Defensa</div>
</button>

</div>

<div class="mt-8 text-center">
  <button @click="$slidev.nav.go(1)" class="px-5 py-2 rounded-full border border-gray-300 bg-gray-100 text-gray-600 text-sm font-medium hover:bg-gray-200 transition-colors cursor-pointer">
    🏠 Volver al Inicio
  </button>
</div>
