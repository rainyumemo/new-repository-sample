<template>
  <div>
    <!-- Hero Section -->
    <section class="pt-32 pb-20 bg-gradient-to-br from-gray-900 via-gray-800 to-primary-900">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        <h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold text-white mb-6">
          成功案例
        </h1>
        <p class="text-xl text-gray-300 max-w-3xl mx-auto">
          看看我们如何帮助客户实现数字化转型，创造真实商业价值
        </p>
      </div>
    </section>

    <!-- Cases Grid -->
    <section class="py-24 bg-white">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
          <div v-for="caseItem in cases" :key="caseItem.title" class="group bg-white rounded-2xl overflow-hidden shadow-lg hover:shadow-2xl transition-all duration-300">
            <!-- Image Placeholder -->
            <div class="h-56 bg-gradient-to-br from-primary-500 to-primary-700 relative overflow-hidden">
              <div class="absolute inset-0 bg-black/20 group-hover:bg-black/10 transition-colors duration-300"></div>
              <div class="absolute bottom-4 left-4">
                <span class="px-3 py-1 bg-white/90 text-primary-700 text-sm font-medium rounded-full">
                  {{ caseItem.industry }}
                </span>
              </div>
            </div>
            
            <!-- Content -->
            <div class="p-8">
              <h3 class="text-xl font-bold text-gray-900 mb-3 group-hover:text-primary-600 transition-colors duration-300">
                {{ caseItem.title }}
              </h3>
              <p class="text-gray-600 mb-6 line-clamp-3">{{ caseItem.description }}</p>
              
              <!-- Results -->
              <div class="grid grid-cols-2 gap-4 mb-6">
                <div class="text-center p-3 bg-gray-50 rounded-lg">
                  <div class="text-2xl font-bold text-primary-600">{{ caseItem.result1.value }}</div>
                  <div class="text-sm text-gray-500">{{ caseItem.result1.label }}</div>
                </div>
                <div class="text-center p-3 bg-gray-50 rounded-lg">
                  <div class="text-2xl font-bold text-primary-600">{{ caseItem.result2.value }}</div>
                  <div class="text-sm text-gray-500">{{ caseItem.result2.label }}</div>
                </div>
              </div>
              
              <!-- Tags -->
              <div class="flex flex-wrap gap-2">
                <span v-for="tag in caseItem.tags" :key="tag" class="px-3 py-1 bg-primary-50 text-primary-700 text-sm rounded-full">
                  {{ tag }}
                </span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Stats Section -->
    <section class="py-24 bg-gray-50">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <h2 class="section-title">客户成果</h2>
          <p class="section-subtitle">
            我们的解决方案为客户创造了显著的商业价值
          </p>
        </div>
        <div class="grid grid-cols-2 lg:grid-cols-4 gap-8">
          <div v-for="stat in stats" :key="stat.label" class="text-center p-8 bg-white rounded-2xl shadow-sm">
            <div class="text-4xl lg:text-5xl font-bold text-primary-600 mb-2">{{ stat.value }}</div>
            <div class="text-gray-600">{{ stat.label }}</div>
          </div>
        </div>
      </div>
    </section>

    <!-- Testimonials Section -->
    <section class="py-24 bg-white">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <h2 class="section-title">客户心声</h2>
          <p class="section-subtitle">
            听听我们的合作伙伴如何评价我们的服务
          </p>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
          <div v-for="testimonial in testimonials" :key="testimonial.author" class="bg-gray-50 p-8 rounded-2xl">
            <div class="flex mb-4">
              <svg v-for="i in 5" :key="i" class="w-5 h-5 text-yellow-400" fill="currentColor" viewBox="0 0 20 20">
                <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
              </svg>
            </div>
            <p class="text-gray-700 mb-6 text-lg leading-relaxed">"{{ testimonial.quote }}"</p>
            <div class="flex items-center">
              <div class="w-12 h-12 bg-gradient-to-br from-primary-500 to-primary-700 rounded-full flex items-center justify-center text-white font-semibold">
                {{ testimonial.author.charAt(0) }}
              </div>
              <div class="ml-4">
                <div class="font-semibold text-gray-900">{{ testimonial.author }}</div>
                <div class="text-sm text-gray-500">{{ testimonial.position }}</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup lang="ts">
const cases = [
  {
    title: '某大型制造企业数字化转型',
    industry: '制造业',
    description: '为某大型制造企业提供全面的数字化转型服务，包括智能制造系统建设、供应链数字化、数据分析平台搭建等，实现了生产效率的显著提升。',
    result1: { value: '40%', label: '效率提升' },
    result2: { value: '30%', label: '成本降低' },
    tags: ['智能制造', '供应链', '数据分析'],
  },
  {
    title: '某金融机构核心系统上云',
    industry: '金融',
    description: '帮助某金融机构完成核心系统的云原生改造，实现了系统的高可用、弹性扩展，同时大幅降低了IT基础设施成本。',
    result1: { value: '99.99%', label: '系统可用性' },
    result2: { value: '50%', label: '成本节省' },
    tags: ['云计算', '云原生', 'DevOps'],
  },
  {
    title: '某零售集团智能客服系统',
    industry: '零售',
    description: '为某零售集团构建基于AI的智能客服系统，实现了7x24小时客户服务，大幅提升了客户满意度和客服效率。',
    result1: { value: '80%', label: '问题解决率' },
    result2: { value: '60%', label: '人工节省' },
    tags: ['人工智能', 'NLP', '客服系统'],
  },
  {
    title: '某物流企业数据中台建设',
    industry: '物流',
    description: '为某物流企业构建企业级数据中台，整合多源数据，实现数据资产化，支撑业务决策和运营优化。',
    result1: { value: '10+', label: '数据源整合' },
    result2: { value: '3x', label: '决策效率' },
    tags: ['数据中台', '数据治理', 'BI'],
  },
  {
    title: '某医疗集团互联网医院平台',
    industry: '医疗',
    description: '为某医疗集团打造互联网医院平台，实现线上线下一体化服务，提升患者就医体验和医院运营效率。',
    result1: { value: '100万+', label: '服务患者' },
    result2: { value: '4.9', label: '用户评分' },
    tags: ['互联网医疗', '移动应用', '云服务'],
  },
  {
    title: '某教育机构智慧校园项目',
    industry: '教育',
    description: '为某教育机构建设智慧校园平台，整合教学、管理、服务等多个系统，打造数字化校园生态。',
    result1: { value: '5万+', label: '覆盖师生' },
    result2: { value: '90%', label: '系统使用率' },
    tags: ['智慧校园', '物联网', '大数据'],
  },
]

const stats = [
  { value: '500+', label: '成功案例' },
  { value: '98%', label: '客户满意度' },
  { value: '40%', label: '平均效率提升' },
  { value: '35%', label: '平均成本节省' },
]

const testimonials = [
  {
    quote: '创新科技的专业能力和服务态度给我们留下了深刻印象。他们不仅技术过硬，更重要的是真正理解我们的业务需求。',
    author: '刘总',
    position: '某制造企业 CEO',
  },
  {
    quote: '与创创新科技合作是我们数字化转型过程中最正确的决定。他们的解决方案帮助我们实现了业务的跨越式发展。',
    author: '赵总',
    position: '某零售集团 CTO',
  },
]
</script>
