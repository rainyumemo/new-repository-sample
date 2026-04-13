<template>
  <nav class="fixed top-0 left-0 right-0 z-50 bg-white/95 backdrop-blur-md border-b border-gray-100 transition-all duration-300"
       :class="{ 'shadow-sm': scrolled }">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between items-center h-16">
        <!-- Logo -->
        <div class="flex-shrink-0 flex items-center">
          <RouterLink to="/" class="flex items-center space-x-2">
            <div class="w-8 h-8 bg-gradient-to-br from-primary-600 to-primary-800 rounded-lg flex items-center justify-center">
              <span class="text-white font-bold text-lg">C</span>
            </div>
            <span class="text-xl font-bold text-gray-900">创新科技</span>
          </RouterLink>
        </div>

        <!-- Desktop Menu -->
        <div class="hidden md:flex items-center space-x-8">
          <RouterLink
            v-for="item in navItems"
            :key="item.path"
            :to="item.path"
            class="text-gray-600 hover:text-primary-600 font-medium transition-colors duration-200"
            :class="{ 'text-primary-600': $route.path === item.path }"
          >
            {{ item.name }}
          </RouterLink>
          <RouterLink to="/contact" class="btn-primary">
            联系我们
          </RouterLink>
        </div>

        <!-- Mobile Menu Button -->
        <div class="md:hidden">
          <button
            @click="mobileMenuOpen = !mobileMenuOpen"
            class="text-gray-600 hover:text-gray-900 focus:outline-none"
          >
            <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path v-if="!mobileMenuOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
              <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
            </svg>
          </button>
        </div>
      </div>
    </div>

    <!-- Mobile Menu -->
    <div v-show="mobileMenuOpen" class="md:hidden bg-white border-t border-gray-100">
      <div class="px-4 pt-2 pb-4 space-y-1">
        <RouterLink
          v-for="item in navItems"
          :key="item.path"
          :to="item.path"
          class="block px-3 py-2 text-base font-medium text-gray-600 hover:text-primary-600 hover:bg-gray-50 rounded-md transition-colors duration-200"
          :class="{ 'text-primary-600 bg-primary-50': $route.path === item.path }"
          @click="mobileMenuOpen = false"
        >
          {{ item.name }}
        </RouterLink>
        <RouterLink
          to="/contact"
          class="block px-3 py-2 text-base font-medium text-primary-600 hover:bg-primary-50 rounded-md transition-colors duration-200"
          @click="mobileMenuOpen = false"
        >
          联系我们
        </RouterLink>
      </div>
    </div>
  </nav>
</template>

<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue'

const navItems = [
  { name: '首页', path: '/' },
  { name: '关于我们', path: '/about' },
  { name: '服务', path: '/services' },
  { name: '案例', path: '/cases' },
]

const scrolled = ref(false)
const mobileMenuOpen = ref(false)

const handleScroll = () => {
  scrolled.value = window.scrollY > 10
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>
