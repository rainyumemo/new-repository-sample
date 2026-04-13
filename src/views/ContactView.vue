<template>
  <div>
    <!-- Hero Section -->
    <section class="pt-32 pb-20 bg-gradient-to-br from-gray-900 via-gray-800 to-primary-900">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        <h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold text-white mb-6">
          联系我们
        </h1>
        <p class="text-xl text-gray-300 max-w-3xl mx-auto">
          期待与您的合作，让我们一起开启数字化转型之旅
        </p>
      </div>
    </section>

    <!-- Contact Section -->
    <section class="py-24 bg-white">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-16">
          <!-- Contact Info -->
          <div>
            <h2 class="text-3xl font-bold text-gray-900 mb-6">获取免费咨询</h2>
            <p class="text-gray-600 text-lg mb-10">
              填写右侧表单，我们的专家团队将在24小时内与您联系，为您提供专业的数字化转型建议。
            </p>
            
            <div class="space-y-6">
              <div class="flex items-start space-x-4">
                <div class="w-12 h-12 bg-primary-100 rounded-lg flex items-center justify-center flex-shrink-0">
                  <svg class="w-6 h-6 text-primary-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
                  </svg>
                </div>
                <div>
                  <h3 class="font-semibold text-gray-900 mb-1">公司地址</h3>
                  <p class="text-gray-600">北京市朝阳区科技园区88号创新大厦18层</p>
                </div>
              </div>
              
              <div class="flex items-start space-x-4">
                <div class="w-12 h-12 bg-primary-100 rounded-lg flex items-center justify-center flex-shrink-0">
                  <svg class="w-6 h-6 text-primary-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                  </svg>
                </div>
                <div>
                  <h3 class="font-semibold text-gray-900 mb-1">电子邮箱</h3>
                  <p class="text-gray-600">contact@chuangxin.tech</p>
                  <p class="text-gray-600">business@chuangxin.tech</p>
                </div>
              </div>
              
              <div class="flex items-start space-x-4">
                <div class="w-12 h-12 bg-primary-100 rounded-lg flex items-center justify-center flex-shrink-0">
                  <svg class="w-6 h-6 text-primary-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
                  </svg>
                </div>
                <div>
                  <h3 class="font-semibold text-gray-900 mb-1">联系电话</h3>
                  <p class="text-gray-600">400-888-8888（客服热线）</p>
                  <p class="text-gray-600">010-8888-8888（总机）</p>
                </div>
              </div>
              
              <div class="flex items-start space-x-4">
                <div class="w-12 h-12 bg-primary-100 rounded-lg flex items-center justify-center flex-shrink-0">
                  <svg class="w-6 h-6 text-primary-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
                  </svg>
                </div>
                <div>
                  <h3 class="font-semibold text-gray-900 mb-1">工作时间</h3>
                  <p class="text-gray-600">周一至周五：9:00 - 18:00</p>
                  <p class="text-gray-600">周六周日：休息</p>
                </div>
              </div>
            </div>
          </div>
          
          <!-- Contact Form -->
          <div class="bg-gray-50 p-8 rounded-2xl">
            <form @submit.prevent="handleSubmit" class="space-y-6">
              <div class="grid grid-cols-1 sm:grid-cols-2 gap-6">
                <div>
                  <label class="block text-sm font-medium text-gray-700 mb-2">姓名 *</label>
                  <input
                    v-model="form.name"
                    type="text"
                    required
                    class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-primary-500 focus:border-transparent transition-all duration-200"
                    placeholder="请输入您的姓名"
                  />
                </div>
                <div>
                  <label class="block text-sm font-medium text-gray-700 mb-2">公司名称</label>
                  <input
                    v-model="form.company"
                    type="text"
                    class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-primary-500 focus:border-transparent transition-all duration-200"
                    placeholder="请输入公司名称"
                  />
                </div>
              </div>
              
              <div class="grid grid-cols-1 sm:grid-cols-2 gap-6">
                <div>
                  <label class="block text-sm font-medium text-gray-700 mb-2">联系电话 *</label>
                  <input
                    v-model="form.phone"
                    type="tel"
                    required
                    class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-primary-500 focus:border-transparent transition-all duration-200"
                    placeholder="请输入联系电话"
                  />
                </div>
                <div>
                  <label class="block text-sm font-medium text-gray-700 mb-2">电子邮箱 *</label>
                  <input
                    v-model="form.email"
                    type="email"
                    required
                    class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-primary-500 focus:border-transparent transition-all duration-200"
                    placeholder="请输入电子邮箱"
                  />
                </div>
              </div>
              
              <div>
                <label class="block text-sm font-medium text-gray-700 mb-2">感兴趣的服务</label>
                <select
                  v-model="form.service"
                  class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-primary-500 focus:border-transparent transition-all duration-200"
                >
                  <option value="">请选择服务类型</option>
                  <option value="consulting">数字化转型咨询</option>
                  <option value="cloud">云计算解决方案</option>
                  <option value="ai">人工智能应用</option>
                  <option value="data">数据分析服务</option>
                  <option value="mobile">移动应用开发</option>
                  <option value="other">其他</option>
                </select>
              </div>
              
              <div>
                <label class="block text-sm font-medium text-gray-700 mb-2">需求描述</label>
                <textarea
                  v-model="form.message"
                  rows="4"
                  class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-primary-500 focus:border-transparent transition-all duration-200 resize-none"
                  placeholder="请简要描述您的需求..."
                ></textarea>
              </div>
              
              <button
                type="submit"
                class="w-full btn-primary py-4 text-lg"
                :disabled="submitting"
              >
                <span v-if="submitting">提交中...</span>
                <span v-else>提交咨询</span>
              </button>
              
              <p class="text-sm text-gray-500 text-center">
                提交即表示您同意我们的隐私政策和服务条款
              </p>
            </form>
          </div>
        </div>
      </div>
    </section>

    <!-- Map Section -->
    <section class="py-24 bg-gray-50">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <h2 class="section-title">来访指引</h2>
          <p class="section-subtitle">
            欢迎莅临创新科技参观交流
          </p>
        </div>
        <div class="bg-gray-200 rounded-2xl h-96 flex items-center justify-center">
          <div class="text-center text-gray-500">
            <svg class="w-16 h-16 mx-auto mb-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
            </svg>
            <p class="text-lg">地图加载中...</p>
            <p class="text-sm mt-2">北京市朝阳区科技园区88号创新大厦</p>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const form = ref({
  name: '',
  company: '',
  phone: '',
  email: '',
  service: '',
  message: '',
})

const submitting = ref(false)

const handleSubmit = async () => {
  submitting.value = true
  
  // Simulate form submission
  await new Promise(resolve => setTimeout(resolve, 1500))
  
  alert('感谢您的咨询！我们的专家团队将在24小时内与您联系。')
  
  // Reset form
  form.value = {
    name: '',
    company: '',
    phone: '',
    email: '',
    service: '',
    message: '',
  }
  
  submitting.value = false
}
</script>
