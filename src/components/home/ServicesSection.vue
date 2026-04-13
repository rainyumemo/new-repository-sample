<template>
  <section class="py-24 bg-gray-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <!-- Section Header -->
      <div class="text-center mb-16">
        <h2 class="section-title">我们的服务</h2>
        <p class="section-subtitle">
          全方位的数字化解决方案，助力企业实现业务创新和增长
        </p>
      </div>
      
      <!-- Services Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div
          v-for="(service, index) in services"
          :key="service.title"
          class="group bg-white rounded-2xl overflow-hidden shadow-sm hover:shadow-xl transition-all duration-300"
        >
          <!-- Image -->
          <div class="h-48 bg-gradient-to-br from-primary-500 to-primary-700 flex items-center justify-center relative overflow-hidden">
            <div class="absolute inset-0 bg-black/10 group-hover:bg-black/0 transition-colors duration-300"></div>
            <svg class="w-20 h-20 text-white/80" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" :d="service.icon" />
            </svg>
          </div>
          
          <!-- Content -->
          <div class="p-8">
            <h3 class="text-xl font-semibold text-gray-900 mb-3 group-hover:text-primary-600 transition-colors duration-300">
              {{ service.title }}
            </h3>
            <p class="text-gray-600 mb-6 leading-relaxed">{{ service.description }}</p>
            
            <!-- Features List -->
            <ul class="space-y-2 mb-6">
              <li v-for="feature in service.features" :key="feature" class="flex items-center text-sm text-gray-500">
                <svg class="w-4 h-4 text-green-500 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                </svg>
                {{ feature }}
              </li>
            </ul>
            
            <!-- Learn More Link -->
            <RouterLink to="/services" class="inline-flex items-center text-primary-600 font-medium hover:text-primary-700 transition-colors duration-200">
              了解更多
              <svg class="ml-1 w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
              </svg>
            </RouterLink>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
const services = [
  {
    title: '数字化转型咨询',
    description: '为企业提供全面的数字化转型战略规划，帮助您制定清晰的数字化路线图。',
    icon: 'M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z',
    features: ['数字化成熟度评估', '战略规划与路线图', '组织架构优化', '变革管理支持'],
  },
  {
    title: '云计算解决方案',
    description: '提供安全、可扩展的云计算服务，助力企业实现IT基础设施的现代化。',
    icon: 'M3 15a4 4 0 004 4h9a5 5 0 10-.1-9.999 5.002 5.002 0 10-9.78 2.096A4.001 4.001 0 003 15z',
    features: ['云架构设计', '云迁移服务', '混合云部署', '云成本优化'],
  },
  {
    title: '人工智能应用',
    description: '利用先进的AI技术，为企业打造智能化的业务流程和决策支持系统。',
    icon: 'M9.75 17L9 20l-1 1h8l-1-1-.75-3M3 13h18M5 17h14a2 2 0 002-2V5a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z',
    features: ['机器学习平台', '智能客服系统', '预测分析', '计算机视觉应用'],
  },
  {
    title: '数据分析服务',
    description: '通过深度数据分析，帮助企业挖掘数据价值，支持数据驱动的业务决策。',
    icon: 'M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z',
    features: ['数据仓库建设', '商业智能平台', '实时数据分析', '数据可视化'],
  },
  {
    title: '移动应用开发',
    description: '为企业打造高质量的移动应用，提升用户体验，拓展业务渠道。',
    icon: 'M12 18h.01M8 21h8a2 2 0 002-2V5a2 2 0 00-2-2H8a2 2 0 00-2 2v14a2 2 0 002 2z',
    features: ['iOS/Android开发', '跨平台解决方案', 'UI/UX设计', '应用运维支持'],
  },
  {
    title: '物联网解决方案',
    description: '构建智能物联网平台，实现设备互联，开启智能制造新时代。',
    icon: 'M8.111 16.404a5.5 5.5 0 017.778 0M12 20h.01m-7.08-7.071c3.904-3.905 10.236-3.905 14.141 0M1.394 9.393c5.857-5.857 15.355-5.857 21.213 0',
    features: ['IoT平台搭建', '设备接入管理', '边缘计算', '智能监控预警'],
  },
]
</script>
