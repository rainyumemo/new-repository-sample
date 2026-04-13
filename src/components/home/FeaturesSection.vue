<template>
  <section class="py-24 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <!-- Section Header -->
      <div class="text-center mb-16">
        <h2 class="section-title">为什么选择我们</h2>
        <p class="section-subtitle">
          我们拥有丰富的行业经验和专业的技术团队，致力于为客户提供最优质的服务
        </p>
      </div>
      
      <!-- Features Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div
          v-for="(feature, index) in features"
          :key="feature.title"
          class="group p-8 bg-gray-50 rounded-2xl hover:bg-white hover:shadow-xl transition-all duration-300 border border-gray-100"
          :class="{ 'animate-slide-up': true }"
          :style="{ animationDelay: `${index * 0.1}s` }"
        >
          <!-- Icon -->
          <div class="w-14 h-14 bg-primary-100 rounded-xl flex items-center justify-center mb-6 group-hover:bg-primary-600 transition-colors duration-300">
            <svg
              class="w-7 h-7 text-primary-600 group-hover:text-white transition-colors duration-300"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" :d="feature.icon" />
            </svg>
          </div>
          
          <!-- Content -->
          <h3 class="text-xl font-semibold text-gray-900 mb-3">{{ feature.title }}</h3>
          <p class="text-gray-600 leading-relaxed">{{ feature.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
const features = [
  {
    title: '专业团队',
    description: '拥有超过10年行业经验的专家团队，深谙各行业的数字化转型需求。',
    icon: 'M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z',
  },
  {
    title: '定制方案',
    description: '根据您的业务特点和需求，量身定制最适合的数字化解决方案。',
    icon: 'M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-3 7h3m-3 4h3m-6-4h.01M9 16h.01',
  },
  {
    title: '持续支持',
    description: '提供7x24小时技术支持，确保您的系统稳定运行，业务不受影响。',
    icon: 'M18.364 5.636l-3.536 3.536m0 5.656l3.536 3.536M9.172 9.172L5.636 5.636m3.536 9.192l-3.536 3.536M21 12a9 9 0 11-18 0 9 9 0 0118 0zm-5 0a4 4 0 11-8 0 4 4 0 018 0z',
  },
  {
    title: '数据安全',
    description: '采用业界领先的安全技术和最佳实践，全方位保护您的数据资产。',
    icon: 'M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z',
  },
  {
    title: '敏捷交付',
    description: '采用敏捷开发方法论，快速迭代，确保项目按时高质量交付。',
    icon: 'M13 10V3L4 14h7v7l9-11h-7z',
  },
  {
    title: '成本优化',
    description: '通过技术创新和流程优化，帮助您降低运营成本，提高投资回报率。',
    icon: 'M12 8c-1.657 0-3 .895-3 2s1.343 2 3 2 3 .895 3 2-1.343 2-3 2m0-8c1.11 0 2.08.402 2.599 1M12 8V7m0 1v8m0 0v1m0-1c-1.11 0-2.08-.402-2.599-1M21 12a9 9 0 11-18 0 9 9 0 0118 0z',
  },
]
</script>
