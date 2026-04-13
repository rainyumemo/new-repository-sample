<template>
  <section class="py-24 bg-primary-900 relative overflow-hidden">
    <!-- Background Pattern -->
    <div class="absolute inset-0 opacity-10">
      <div class="absolute inset-0" style="background-image: radial-gradient(circle at 2px 2px, white 1px, transparent 0); background-size: 32px 32px;"></div>
    </div>
    
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
      <div class="grid grid-cols-2 lg:grid-cols-4 gap-8">
        <div
          v-for="(stat, index) in stats"
          :key="stat.label"
          class="text-center"
        >
          <div class="text-4xl sm:text-5xl lg:text-6xl font-bold text-white mb-2">
            <span ref="statRefs" :data-target="stat.value">0</span>{{ stat.suffix }}
          </div>
          <div class="text-primary-200 text-sm sm:text-base">{{ stat.label }}</div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref, onMounted } from 'vue'

const stats = [
  { value: 500, suffix: '+', label: '服务企业' },
  { value: 98, suffix: '%', label: '客户满意度' },
  { value: 50, suffix: '+', label: '技术专家' },
  { value: 10, suffix: '年', label: '行业经验' },
]

const statRefs = ref<HTMLElement[]>([])

onMounted(() => {
  const observer = new IntersectionObserver((entries) => {
    entries.forEach((entry) => {
      if (entry.isIntersecting) {
        const target = entry.target as HTMLElement
        const targetValue = parseInt(target.dataset.target || '0')
        animateValue(target, 0, targetValue, 2000)
        observer.unobserve(target)
      }
    })
  }, { threshold: 0.5 })

  statRefs.value.forEach((ref) => {
    if (ref) observer.observe(ref)
  })
})

function animateValue(obj: HTMLElement, start: number, end: number, duration: number) {
  let startTimestamp: number | null = null
  const step = (timestamp: number) => {
    if (!startTimestamp) startTimestamp = timestamp
    const progress = Math.min((timestamp - startTimestamp) / duration, 1)
    const easeOutQuart = 1 - Math.pow(1 - progress, 4)
    obj.innerHTML = Math.floor(progress * (end - start) + start).toString()
    if (progress < 1) {
      window.requestAnimationFrame(step)
    }
  }
  window.requestAnimationFrame(step)
}
</script>
