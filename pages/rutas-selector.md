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

<div class="grid grid-cols-2 gap-8 mt-8 max-w-3xl mx-auto">

<button @click="$slidev.nav.go(9)" class="p-8 rounded-2xl border-2 border-teal-300 bg-teal-50 hover:bg-teal-100 hover:scale-105 transition-all cursor-pointer text-center shadow-sm">
  <div class="text-6xl mb-4">🗄️</div>
  <div class="text-teal-700 font-bold text-xl">Desarrollador de Bases de Datos</div>
  <div class="text-sm text-gray-500 mt-2">SQL · Modelado · Optimización · Big Data</div>
  <div class="mt-4 text-xs text-teal-600 font-medium">Ver ruta →</div>
</button>

<button @click="$slidev.nav.go(16)" class="p-8 rounded-2xl border-2 border-blue-300 bg-blue-50 hover:bg-blue-100 hover:scale-105 transition-all cursor-pointer text-center shadow-sm">
  <div class="text-6xl mb-4">⚙️</div>
  <div class="text-blue-700 font-bold text-xl">Desarrollador Backend</div>
  <div class="text-sm text-gray-500 mt-2">APIs · Microservicios · Seguridad · Cloud</div>
  <div class="mt-4 text-xs text-blue-600 font-medium">Ver ruta →</div>
</button>

</div>

<div class="mt-8 text-center">
  <button @click="$slidev.nav.go(1)" class="px-5 py-2 rounded-full border border-gray-300 bg-gray-100 text-gray-600 text-sm font-medium hover:bg-gray-200 transition-colors cursor-pointer">
    🏠 Volver al Inicio
  </button>
</div>
