<template>
  <div>
    <!-- Hero Section -->
    <section class="pt-32 pb-20 bg-gradient-to-br from-gray-900 via-gray-800 to-primary-900">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        <h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold text-white mb-6">
          关于创新科技
        </h1>
        <p class="text-xl text-gray-300 max-w-3xl mx-auto">
          我们是一家专注于企业数字化转型的科技公司，致力于用技术创新推动商业进步
        </p>
      </div>
    </section>

    <!-- Mission Section -->
    <section class="py-24 bg-white">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 items-center">
          <div>
            <h2 class="section-title">我们的使命</h2>
            <p class="text-gray-600 text-lg leading-relaxed mb-6">
              在数字化浪潮席卷全球的今天，创新科技始终站在技术前沿，帮助企业把握数字化机遇，实现业务创新和增长。
            </p>
            <p class="text-gray-600 text-lg leading-relaxed mb-6">
              我们相信，技术的价值在于解决实际问题。因此，我们不仅提供先进的技术解决方案，更注重深入理解客户的业务需求，确保每一个项目都能为客户创造真实的商业价值。
            </p>
            <div class="flex items-center space-x-4">
              <div class="w-12 h-12 bg-primary-100 rounded-full flex items-center justify-center">
                <svg class="w-6 h-6 text-primary-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z" />
                </svg>
              </div>
              <div>
                <div class="font-semibold text-gray-900">创新驱动</div>
                <div class="text-sm text-gray-500">持续探索前沿技术</div>
              </div>
            </div>
          </div>
          <div class="relative">
            <div class="aspect-w-4 aspect-h-3 bg-gradient-to-br from-primary-500 to-primary-700 rounded-2xl flex items-center justify-center">
              <div class="text-center text-white p-8">
                <div class="text-6xl font-bold mb-4">10+</div>
                <div class="text-xl">年行业深耕</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Values Section -->
    <section class="py-24 bg-gray-50">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <h2 class="section-title">核心价值观</h2>
          <p class="section-subtitle">
            这些价值观指引着我们的每一个决策和行动
          </p>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
          <div v-for="value in values" :key="value.title" class="bg-white p-8 rounded-2xl shadow-sm text-center">
            <div class="w-16 h-16 bg-primary-100 rounded-2xl flex items-center justify-center mx-auto mb-6">
              <svg class="w-8 h-8 text-primary-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" :d="value.icon" />
              </svg>
            </div>
            <h3 class="text-xl font-semibold text-gray-900 mb-3">{{ value.title }}</h3>
            <p class="text-gray-600">{{ value.description }}</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Team Section -->
    <section class="py-24 bg-white">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <h2 class="section-title">核心团队</h2>
          <p class="section-subtitle">
            由行业资深专家组成的专业团队
          </p>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
          <div v-for="member in team" :key="member.name" class="text-center">
            <div class="w-32 h-32 bg-gradient-to-br from-primary-400 to-primary-600 rounded-full mx-auto mb-4 flex items-center justify-center text-white text-3xl font-bold">
              {{ member.name.charAt(0) }}
            </div>
            <h3 class="text-lg font-semibold text-gray-900">{{ member.name }}</h3>
            <p class="text-primary-600 mb-2">{{ member.position }}</p>
            <p class="text-gray-500 text-sm">{{ member.description }}</p>
          </div>
        </div>
      </div>
    </section>

    <!-- History Section -->
    <section class="py-24 bg-gray-50">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <h2 class="section-title">发展历程</h2>
          <p class="section-subtitle">
            创新科技的成长之路
          </p>
        </div>
        <div class="relative">
          <div class="absolute left-1/2 transform -translate-x-1/2 h-full w-0.5 bg-primary-200"></div>
          <div class="space-y-12">
            <div v-for="(milestone, index) in milestones" :key="milestone.year" class="relative">
              <div class="flex items-center" :class="index % 2 === 0 ? 'flex-row' : 'flex-row-reverse'">
                <div class="w-1/2 px-8" :class="index % 2 === 0 ? 'text-right' : 'text-left'">
                  <div class="bg-white p-6 rounded-xl shadow-sm">
                    <div class="text-primary-600 font-bold text-lg mb-2">{{ milestone.year }}</div>
                    <h3 class="font-semibold text-gray-900 mb-2">{{ milestone.title }}</h3>
                    <p class="text-gray-600 text-sm">{{ milestone.description }}</p>
                  </div>
                </div>
                <div class="absolute left-1/2 transform -translate-x-1/2 w-4 h-4 bg-primary-600 rounded-full border-4 border-white"></div>
                <div class="w-1/2 px-8"></div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup lang="ts">
const values = [
  {
    title: '客户至上',
    description: '始终以客户需求为中心，提供超越期望的服务体验。',
    icon: 'M14.828 14.828a4 4 0 01-5.656 0M9 10h.01M15 10h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z',
  },
  {
    title: '追求卓越',
    description: '不断挑战自我，追求技术和服务的极致完美。',
    icon: 'M5 3v4M3 5h4M6 17v4m-2-2h4m5-16l2.286 6.857L21 12l-5.714 2.143L13 21l-2.286-6.857L5 12l5.714-2.143L13 3z',
  },
  {
    title: '诚信透明',
    description: '坚持诚信经营，与客户建立长期信任的合作关系。',
    icon: 'M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z',
  },
  {
    title: '协作共赢',
    description: '与客户、合作伙伴携手共进，创造更大价值。',
    icon: 'M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z',
  },
]

const team = [
  {
    name: '陈明',
    position: '创始人 & CEO',
    description: '20年科技行业经验，曾任多家知名企业技术高管',
  },
  {
    name: '林晓',
    position: '技术总监',
    description: '云计算和AI领域专家，主导多个大型数字化转型项目',
  },
  {
    name: '张伟',
    position: '产品总监',
    description: '专注于企业级产品设计，拥有丰富的B端产品经验',
  },
  {
    name: '王芳',
    position: '运营总监',
    description: '擅长企业运营优化，帮助客户实现业务增长',
  },
]

const milestones = [
  {
    year: '2015',
    title: '公司成立',
    description: '创新科技在北京成立，专注于企业数字化服务',
  },
  {
    year: '2017',
    title: '业务拓展',
    description: '服务客户突破100家，业务覆盖全国主要城市',
  },
  {
    year: '2019',
    title: '技术升级',
    description: '成立AI实验室，推出智能客服和预测分析产品',
  },
  {
    year: '2021',
    title: '战略转型',
    description: '完成B轮融资，全面布局云计算和物联网领域',
  },
  {
    year: '2024',
    title: '行业领先',
    description: '服务企业超过500家，成为行业领先的数字化解决方案提供商',
  },
]
</script>
