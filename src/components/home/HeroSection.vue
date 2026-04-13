<template>
  <section class="relative min-h-screen flex items-center justify-center overflow-hidden">
    <!-- Background Image -->
    <div class="absolute inset-0">
      <img 
        src="/images/hero-bg.jpg" 
        alt="背景" 
        class="w-full h-full object-cover"
      />
      <div class="absolute inset-0 bg-gray-900/70"></div>
    </div>
    <!-- Background Pattern -->
    <div class="absolute inset-0 opacity-20">
      <div class="absolute inset-0" style="background-image: radial-gradient(circle at 1px 1px, white 1px, transparent 0); background-size: 40px 40px;"></div>
    </div>
    
    <!-- Animated Gradient Orbs -->
    <div class="absolute top-1/4 left-1/4 w-96 h-96 bg-primary-500/30 rounded-full blur-3xl animate-pulse"></div>
    <div class="absolute bottom-1/4 right-1/4 w-80 h-80 bg-purple-500/20 rounded-full blur-3xl animate-pulse" style="animation-delay: 1s;"></div>
    <div class="absolute top-1/2 right-1/3 w-64 h-64 bg-blue-500/20 rounded-full blur-3xl animate-pulse" style="animation-delay: 2s;"></div>
    
    <!-- Content -->
    <div class="relative z-10 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
      <div class="animate-fade-in">
        <!-- Badge -->
        <div class="inline-flex items-center px-4 py-2 rounded-full bg-white/10 backdrop-blur-sm border border-white/20 mb-8">
          <span class="flex h-2 w-2 rounded-full bg-green-400 mr-2 animate-pulse"></span>
          <span class="text-white/90 text-sm font-medium">现已为 500+ 企业提供数字化转型服务</span>
        </div>
        
        <!-- Main Heading -->
        <h1 class="text-4xl sm:text-5xl md:text-6xl lg:text-7xl font-bold text-white mb-6 leading-tight">
          引领企业<br />
          <span class="text-gradient bg-gradient-to-r from-primary-400 to-purple-400 bg-clip-text text-transparent">
            数字化转型
          </span>
        </h1>
        
        <!-- Subtitle -->
        <p class="text-lg sm:text-xl text-gray-300 mb-10 max-w-3xl mx-auto leading-relaxed">
          我们提供全方位的技术解决方案，从战略规划到落地实施，
          助力您的企业在数字时代保持竞争优势，实现可持续增长。
        </p>
        
        <!-- CTA Buttons -->
        <div class="flex flex-col sm:flex-row items-center justify-center gap-4">
          <RouterLink to="/contact" class="btn-primary text-lg px-8 py-4">
            开始您的转型之旅
            <svg class="ml-2 w-5 h-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7l5 5m0 0l-5 5m5-5H6" />
            </svg>
          </RouterLink>
          <RouterLink to="/services" class="btn-secondary text-lg px-8 py-4">
            了解我们的服务
          </RouterLink>
        </div>
      </div>
      
      <!-- Trust Badges -->
      <div class="mt-20 animate-slide-up" style="animation-delay: 0.3s;">
        <p class="text-gray-400 text-sm mb-6">受到众多行业领先企业的信赖</p>
        <div class="flex flex-wrap items-center justify-center gap-8 opacity-60">
          <div v-for="i in 5" :key="i" class="h-8 w-32 bg-white/20 rounded"></div>
        </div>
      </div>
    </div>
    
    <!-- Scroll Indicator -->
    <div class="absolute bottom-8 left-1/2 transform -translate-x-1/2 animate-bounce">
      <svg class="w-6 h-6 text-white/50" fill="none" viewBox="0 0 24 24" stroke="currentColor">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3" />
      </svg>
    </div>
  </section>
</template>
