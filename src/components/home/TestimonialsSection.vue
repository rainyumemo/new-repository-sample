<template>
  <section class="py-24 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <!-- Section Header -->
      <div class="text-center mb-16">
        <h2 class="section-title">客户评价</h2>
        <p class="section-subtitle">
          听听我们的客户怎么说，他们的成功是我们最大的动力
        </p>
      </div>
      
      <!-- Testimonials Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div
          v-for="(testimonial, index) in testimonials"
          :key="testimonial.author"
          class="bg-gray-50 rounded-2xl p-8 relative"
        >
          <!-- Quote Icon -->
          <div class="absolute top-6 right-6 text-primary-200">
            <svg class="w-10 h-10" fill="currentColor" viewBox="0 0 24 24">
              <path d="M14.017 21v-7.391c0-5.704 3.731-9.57 8.983-10.609l.995 2.151c-2.432.917-3.995 3.638-3.995 5.849h4v10h-9.983zm-14.017 0v-7.391c0-5.704 3.748-9.57 9-10.609l.996 2.151c-2.433.917-3.996 3.638-3.996 5.849h3.983v10h-9.983z"/>
            </svg>
          </div>
          
          <!-- Rating -->
          <div class="flex mb-4">
            <svg v-for="i in 5" :key="i" class="w-5 h-5 text-yellow-400" fill="currentColor" viewBox="0 0 20 20">
              <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
            </svg>
          </div>
          
          <!-- Quote -->
          <p class="text-gray-700 mb-6 leading-relaxed">{{ testimonial.quote }}</p>
          
          <!-- Author -->
          <div class="flex items-center">
            <div class="w-12 h-12 bg-gradient-to-br from-primary-500 to-primary-700 rounded-full flex items-center justify-center text-white font-semibold text-lg">
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
</template>

<script setup lang="ts">
const testimonials = [
  {
    quote: '创新科技帮助我们完成了数字化转型，业务效率提升了40%。他们的专业团队不仅技术过硬，而且非常了解我们的业务需求。',
    author: '张明',
    position: '某大型制造企业 CTO',
  },
  {
    quote: '从项目启动到上线，创新科技展现了极高的专业素养。他们的云解决方案帮助我们节省了大量的IT成本。',
    author: '李华',
    position: '某金融机构 技术总监',
  },
  {
    quote: '选择创新科技是我们做过的最正确的决定之一。他们的AI解决方案为我们的客户服务带来了革命性的改变。',
    author: '王芳',
    position: '某电商平台 运营总监',
  },
]
</script>
