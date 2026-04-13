<template>
  <div>
    <!-- Hero Section -->
    <section class="pt-32 pb-20 bg-gradient-to-br from-gray-900 via-gray-800 to-primary-900">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        <h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold text-white mb-6">
          我们的服务
        </h1>
        <p class="text-xl text-gray-300 max-w-3xl mx-auto">
          全方位的数字化解决方案，助力企业实现业务创新和增长
        </p>
      </div>
    </section>

    <!-- Services Detail Section -->
    <section class="py-24 bg-white">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="space-y-24">
          <div v-for="(service, index) in services" :key="service.title" 
               class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center"
               :class="index % 2 === 1 ? 'lg:flex-row-reverse' : ''">
            <div :class="index % 2 === 1 ? 'lg:order-2' : ''">
              <div class="w-16 h-16 bg-primary-100 rounded-2xl flex items-center justify-center mb-6">
                <svg class="w-8 h-8 text-primary-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" :d="service.icon" />
                </svg>
              </div>
              <h2 class="text-3xl font-bold text-gray-900 mb-4">{{ service.title }}</h2>
              <p class="text-gray-600 text-lg mb-6 leading-relaxed">{{ service.description }}</p>
              <ul class="space-y-3 mb-8">
                <li v-for="feature in service.features" :key="feature" class="flex items-center text-gray-700">
                  <svg class="w-5 h-5 text-green-500 mr-3" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  {{ feature }}
                </li>
              </ul>
              <RouterLink to="/contact" class="btn-primary">
                咨询此服务
              </RouterLink>
            </div>
            <div :class="index % 2 === 1 ? 'lg:order-1' : ''">
              <div class="aspect-w-16 aspect-h-10 bg-gradient-to-br from-primary-500 to-primary-700 rounded-2xl flex items-center justify-center">
                <svg class="w-32 h-32 text-white/50" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1" :d="service.icon" />
                </svg>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Process Section -->
    <section class="py-24 bg-gray-50">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <h2 class="section-title">服务流程</h2>
          <p class="section-subtitle">
            标准化的服务流程，确保项目高质量交付
          </p>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
          <div v-for="(step, index) in process" :key="step.title" class="relative">
            <div class="bg-white p-8 rounded-2xl shadow-sm text-center h-full">
              <div class="w-16 h-16 bg-primary-600 text-white rounded-full flex items-center justify-center text-2xl font-bold mx-auto mb-6">
                {{ index + 1 }}
              </div>
              <h3 class="text-xl font-semibold text-gray-900 mb-3">{{ step.title }}</h3>
              <p class="text-gray-600">{{ step.description }}</p>
            </div>
            <div v-if="index < process.length - 1" class="hidden lg:block absolute top-1/2 -right-4 transform -translate-y-1/2 z-10">
              <svg class="w-8 h-8 text-primary-300" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
              </svg>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- CTA Section -->
    <section class="py-24 bg-primary-900">
      <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        <h2 class="text-3xl sm:text-4xl font-bold text-white mb-6">
          需要定制化解决方案？
        </h2>
        <p class="text-xl text-primary-100 mb-10">
          我们的专家团队将根据您的具体需求，为您量身定制最适合的解决方案
        </p>
        <RouterLink to="/contact" class="inline-flex items-center justify-center px-8 py-4 bg-white text-primary-600 font-semibold rounded-lg hover:bg-gray-100 transition-colors duration-200 text-lg">
          联系我们
          <svg class="ml-2 w-5 h-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7l5 5m0 0l-5 5m5-5H6" />
          </svg>
        </RouterLink>
      </div>
    </section>
  </div>
</template>

<script setup lang="ts">
const services = [
  {
    title: '数字化转型咨询',
    description: '我们的咨询团队将深入了解您的业务现状和目标，为您制定全面的数字化转型战略。从现状评估到路线图规划，我们提供端到端的咨询服务，确保您的转型之旅方向正确、步伐稳健。',
    icon: 'M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z',
    features: [
      '数字化成熟度评估与诊断',
      '转型战略与路线图规划',
      '组织架构与流程优化建议',
      '技术选型与架构设计',
    ],
  },
  {
    title: '云计算解决方案',
    description: '我们提供从云架构设计到迁移实施的全栈云服务。无论是公有云、私有云还是混合云，我们都能帮助您构建安全、可扩展、高性价比的云计算环境。',
    icon: 'M3 15a4 4 0 004 4h9a5 5 0 10-.1-9.999 5.002 5.002 0 10-9.78 2.096A4.001 4.001 0 003 15z',
    features: [
      '云架构设计与规划',
      '云迁移与实施服务',
      '混合云与多云管理',
      '云成本优化与治理',
    ],
  },
  {
    title: '人工智能应用',
    description: '利用机器学习和深度学习技术，我们帮助企业构建智能化的业务系统。从智能客服到预测分析，从图像识别到自然语言处理，让AI为您的业务赋能。',
    icon: 'M9.75 17L9 20l-1 1h8l-1-1-.75-3M3 13h18M5 17h14a2 2 0 002-2V5a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z',
    features: [
      '机器学习平台搭建',
      '智能客服与对话系统',
      '预测分析与智能决策',
      '计算机视觉应用开发',
    ],
  },
  {
    title: '数据分析服务',
    description: '数据是新时代的石油。我们帮助企业建立完整的数据体系，从数据采集、存储到分析和可视化，让数据真正成为驱动业务增长的引擎。',
    icon: 'M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z',
    features: [
      '数据仓库与数据湖建设',
      '商业智能与报表平台',
      '实时数据分析与流处理',
      '数据可视化与大屏展示',
    ],
  },
]

const process = [
  {
    title: '需求分析',
    description: '深入了解您的业务需求和痛点，明确项目目标和范围',
  },
  {
    title: '方案设计',
    description: '基于需求分析，设计最优的技术方案和实施路线图',
  },
  {
    title: '开发实施',
    description: '采用敏捷开发方法，快速迭代，确保高质量交付',
  },
  {
    title: '运维支持',
    description: '提供7x24小时运维支持，确保系统稳定运行',
  },
]
</script>
