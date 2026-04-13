<template>
  <section class="py-24 bg-gradient-to-br from-primary-600 to-primary-800 relative overflow-hidden">
    <!-- Background Pattern -->
    <div class="absolute inset-0 opacity-10">
      <div class="absolute inset-0" style="background-image: radial-gradient(circle at 2px 2px, white 1px, transparent 0); background-size: 40px 40px;"></div>
    </div>
    
    <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-center relative z-10">
      <h2 class="text-3xl sm:text-4xl lg:text-5xl font-bold text-white mb-6">
        准备好开始您的<br />数字化转型之旅了吗？
      </h2>
      <p class="text-xl text-primary-100 mb-10 max-w-2xl mx-auto">
        立即联系我们，获取免费的数字化成熟度评估和定制化解决方案建议。
      </p>
      <div class="flex flex-col sm:flex-row items-center justify-center gap-4">
        <RouterLink to="/contact" class="inline-flex items-center justify-center px-8 py-4 bg-white text-primary-600 font-semibold rounded-lg hover:bg-gray-100 transition-colors duration-200 text-lg">
          免费咨询
          <svg class="ml-2 w-5 h-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7l5 5m0 0l-5 5m5-5H6" />
          </svg>
        </RouterLink>
        <a href="tel:400-888-8888" class="inline-flex items-center justify-center px-8 py-4 border-2 border-white text-white font-semibold rounded-lg hover:bg-white/10 transition-colors duration-200 text-lg">
          <svg class="mr-2 w-5 h-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
          </svg>
          400-888-8888
        </a>
      </div>
    </div>
  </section>
</template>
