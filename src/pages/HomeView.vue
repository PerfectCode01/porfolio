<template>
  <main class="px-72 h-screen bg-black overflow-hidden">
    <div class="text-white flex justify-between py-5">
      <p class="font-bold text-2xl">JAPHET BAZ</p>
      <div class="flex gap-5 font-bold">
        <div class="cursor-pointer">Home</div>
        <div class="cursor-pointer">Work</div>
        <div class="cursor-pointer">
          <div>About</div>
        </div>
      </div>
    </div>

    <div class="h-full flex justify-center items-center">
      <div class="text-center flex flex-col items-center justify-center">
        <div class="pb-5">
          <h2 ref="title" class="text-7xl font-bold text-white">WEB & MOBILE Developer<br /></h2>
        </div>
        <p ref="desc" class="text-gray-500 w-1/2 text-center">
          passionate with experience in web and mobile application development. I am constantly
          looking for new challenges to improve my skills and provide innovative solutions.
        </p>
        <button
          ref="btn"
          class="border border-white px-3 py-2 mt-10 rounded-md font-bold text-white"
        >
          SEE MY WORK
        </button>
      </div>

      <!-- Footer -->
      <div class="fixed bottom-0 left-0 w-full text-white text-center py-10">
        <div class="flex gap-3 justify-center">
          <a href="" ref="box1">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 24 24"
              width="24"
              height="24"
              fill="currentColor"
            >
              <path
                d="M19 0h-14c-2.75 0-5 2.25-5 5v14c0 2.75 2.25 5 5 5h14c2.75 0 5-2.25 5-5v-14c0-2.75-2.25-5-5-5zm-11.7 19h-2.8v-8h2.8v8zm-1.4-9.25c-.9 0-1.6-.75-1.6-1.65 0-.9.7-1.65 1.6-1.65s1.6.75 1.6 1.65c0 .9-.7 1.65-1.6 1.65zm13.1 9.25h-2.8v-4.4c0-1.1-.4-1.8-1.3-1.8-.7 0-1.1.45-1.3.9-.1.2-.1.45-.1.7v4.6h-2.8v-8h2.8v1.15c.4-.6 1.1-1.15 2.3-1.15 1.7 0 3 1.1 3 3.45v4.55z"
              />
            </svg>
          </a>
          <a href="" ref="box2">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 24 24"
              width="24"
              height="24"
              fill="currentColor"
            >
              <path
                d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.387.6.113.82-.258.82-.577v-2.234c-3.338.726-4.033-1.415-4.033-1.415-.546-1.387-1.333-1.757-1.333-1.757-1.086-.744.083-.729.083-.729 1.205.084 1.838 1.235 1.838 1.235 1.07 1.835 2.809 1.304 3.495.997.108-.776.418-1.304.763-1.605-2.665-.3-5.466-1.335-5.466-5.93 0-1.31.469-2.381 1.236-3.221-.124-.303-.536-1.52.117-3.176 0 0 1.008-.322 3.3 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.29-1.552 3.295-1.23 3.295-1.23.655 1.656.243 2.873.12 3.176.77.84 1.234 1.911 1.234 3.221 0 4.61-2.805 5.625-5.475 5.92.43.372.823 1.102.823 2.222v3.293c0 .32.217.694.825.577 4.765-1.587 8.2-6.084 8.2-11.386 0-6.627-5.373-12-12-12z"
              />
            </svg>
          </a>
          <a href="" ref="box3">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 24 24"
              width="24"
              height="24"
              fill="currentColor"
            >
              <path
                d="M20 4H4c-1.1 0-2 .9-2 2v12c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm-.4 2L12 11.65 4.4 6h15.2zM4 18V8.67l7.6 5.12c.22.15.48.23.74.23s.52-.08.74-.23L20 8.67V18H4z"
              />
            </svg>
          </a>
        </div>
        <div class="py-5">
          <p class="text-center text-gray-500 text-sm">
            &copy; 2024 Japhet Baz. Tous droits réservés.
          </p>
        </div>
      </div>
    </div>
  </main>
</template>
<script setup>
import { ref, onMounted } from 'vue'
import { gsap } from 'gsap'

// Créez une référence pour l'élément
const title = ref(null)
const desc = ref(null)
const btn = ref(null)

const box1 = ref(null)
const box2 = ref(null)
const box3 = ref(null)

onMounted(() => {
  // Animez l'élément avec GSAP
  gsap.from(title.value, {
    duration: 1,
    y: -30,
    ease: 'power2.out'
  })

  gsap.from(desc.value, {
    duration: 2,
    y: -30,
    ease: 'power2.out'
  })

  gsap.from(btn.value, {
    duration: 3,
    y: -30,
    ease: 'power2.out'
  })

  btn.value.addEventListener('mouseenter', () => {
    gsap.to(btn.value, {
      duration: 0.5,
      background: 'linear-gradient(90deg, #9333ea, #1e3a8a)' // Gradient inversé
    })
  })

  btn.value.addEventListener('mouseleave', () => {
    gsap.to(btn.value, {
      duration: 0.5,
      background: 'linear-gradient(90deg, #1e3a8a, #9333ea)' // Gradient initial
    })
  })

  gsap.from(box1.value, { opacity: 0, y: 100, duration: 1 })
  gsap.from(box2.value, { opacity: 0, y: 100, duration: 1, delay: 0.5 })
  gsap.from(box3.value, { opacity: 0, y: 100, duration: 1, delay: 1 })

  box1.value.addEventListener('mouseenter', () => {
    gsap.to(box1.value, { duration: 1, y: -10 })
  })

  box1.value.addEventListener('mouseleave', () => {
    gsap.to(box1.value, { duration: 1, y: 0 }) // Retour à la position initiale
  })
})
</script>
