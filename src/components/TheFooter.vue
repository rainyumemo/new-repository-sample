<template>
  <footer class="bg-gray-900 text-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
        <!-- Company Info -->
        <div>
          <div class="flex items-center space-x-2 mb-4">
            <div class="w-8 h-8 bg-gradient-to-br from-primary-600 to-primary-800 rounded-lg flex items-center justify-center">
              <span class="text-white font-bold text-lg">C</span>
            </div>
            <span class="text-xl font-bold">创新科技</span>
          </div>
          <p class="text-gray-400 text-sm leading-relaxed">
            致力于为企业提供领先的数字化转型解决方案，助力企业在数字时代蓬勃发展。
          </p>
        </div>

        <!-- Quick Links -->
        <div>
          <h3 class="text-lg font-semibold mb-4">快速链接</h3>
          <ul class="space-y-2">
            <li v-for="item in quickLinks" :key="item.path">
              <RouterLink :to="item.path" class="text-gray-400 hover:text-white transition-colors duration-200">
                {{ item.name }}
              </RouterLink>
            </li>
          </ul>
        </div>

        <!-- Services -->
        <div>
          <h3 class="text-lg font-semibold mb-4">服务</h3>
          <ul class="space-y-2">
            <li v-for="service in services" :key="service">
              <span class="text-gray-400">{{ service }}</span>
            </li>
          </ul>
        </div>

        <!-- Contact -->
        <div>
          <h3 class="text-lg font-semibold mb-4">联系我们</h3>
          <ul class="space-y-3">
            <li class="flex items-start space-x-3">
              <svg class="w-5 h-5 text-primary-500 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
              </svg>
              <span class="text-gray-400 text-sm">北京市朝阳区科技园区88号</span>
            </li>
            <li class="flex items-center space-x-3">
              <svg class="w-5 h-5 text-primary-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
              </svg>
              <span class="text-gray-400 text-sm">contact@chuangxin.tech</span>
            </li>
            <li class="flex items-center space-x-3">
              <svg class="w-5 h-5 text-primary-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
              </svg>
              <span class="text-gray-400 text-sm">400-888-8888</span>
            </li>
          </ul>
        </div>
      </div>

      <!-- Bottom Bar -->
      <div class="border-t border-gray-800 mt-12 pt-8 flex flex-col md:flex-row justify-between items-center">
        <p class="text-gray-500 text-sm">
          © 2025 创新科技. 保留所有权利.
        </p>
        <div class="flex space-x-6 mt-4 md:mt-0">
          <a href="#" class="text-gray-400 hover:text-white transition-colors duration-200">
            <span class="sr-only">微信</span>
            <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
              <path d="M8.691 2.188C3.891 2.188 0 5.476 0 9.53c0 2.212 1.17 4.203 3.002 5.55a.59.59 0 0 1 .213.665l-.39 1.48c-.019.07-.048.141-.048.213 0 .163.13.295.29.295a.326.326 0 0 0 .167-.054l1.903-1.114a.864.864 0 0 1 .717-.098 10.16 10.16 0 0 0 2.837.403c.276 0 .543-.027.811-.05-.857-2.578.157-4.972 1.932-6.446 1.703-1.415 3.882-1.98 5.853-1.838-.576-3.583-4.196-6.348-8.596-6.348zM5.785 5.991c.642 0 1.162.529 1.162 1.18a1.17 1.17 0 0 1-1.162 1.178A1.17 1.17 0 0 1 4.623 7.17c0-.651.52-1.18 1.162-1.18zm5.813 0c.642 0 1.162.529 1.162 1.18a1.17 1.17 0 0 1-1.162 1.178 1.17 1.17 0 0 1-1.162-1.178c0-.651.52-1.18 1.162-1.18zm5.34 2.867c-1.797-.052-3.746.512-5.28 1.786-1.72 1.428-2.687 3.72-1.78 6.22.942 2.453 3.666 4.229 6.884 4.229.826 0 1.622-.12 2.361-.336a.722.722 0 0 1 .598.082l1.584.926a.272.272 0 0 0 .14.045c.134 0 .24-.111.24-.247 0-.06-.023-.12-.038-.177l-.327-1.233a.582.582 0 0 1-.023-.156.49.49 0 0 1 .201-.398C23.024 18.48 24 16.82 24 14.98c0-3.21-2.931-5.837-6.656-6.088V8.89c-.135-.01-.269-.03-.407-.03zm-2.53 3.274c.535 0 .969.44.969.982a.976.976 0 0 1-.969.983.976.976 0 0 1-.969-.983c0-.542.434-.982.97-.982zm4.844 0c.535 0 .969.44.969.982a.976.976 0 0 1-.969.983.976.976 0 0 1-.969-.983c0-.542.434-.982.969-.982z"/>
            </svg>
          </a>
          <a href="#" class="text-gray-400 hover:text-white transition-colors duration-200">
            <span class="sr-only">微博</span>
            <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
              <path d="M10.098 20.323c-3.977.391-7.414-1.406-7.672-4.02-.259-2.609 2.759-5.047 6.74-5.441 3.979-.394 7.413 1.404 7.671 4.018.259 2.6-2.759 5.049-6.739 5.443zM9.05 17.219c-.384.616-1.208.884-1.829.602-.612-.279-.793-.991-.406-1.593.379-.595 1.176-.861 1.793-.601.622.263.82.972.442 1.592zm1.27-1.627c-.141.237-.449.353-.689.253-.236-.09-.313-.361-.177-.586.138-.227.436-.346.672-.24.239.09.315.36.194.573zm.176-2.719c-1.893-.493-4.033.45-4.857 2.118-.836 1.704-.026 3.591 1.886 4.21 1.983.64 4.318-.341 5.132-2.179.8-1.793-.201-3.642-2.161-4.149zm7.563-1.224c-.346-.105-.579-.18-.401-.649.386-1.031.425-1.922.003-2.555-.789-1.187-2.924-1.123-5.383-.034 0 0-.768.334-.571-.271.378-1.207.32-2.217-.266-2.8-1.331-1.32-4.869.047-7.91 3.052C1.904 10.491 0 12.676 0 14.524c0 3.534 4.532 5.686 8.97 5.686 5.807 0 9.676-3.371 9.676-6.052 0-1.614-1.363-2.528-2.587-2.509zm2.043-6.667c-.881-.975-2.182-1.349-3.353-1.149a.75.75 0 1 0 .244 1.48c.729-.12 1.492.09 2.01.663.52.573.684 1.346.458 2.058a.75.75 0 1 0 1.424.468c.343-1.048.084-2.258-.783-3.52zm2.208-2.339C20.257.791 17.88.074 15.582.515a.75.75 0 0 0 .271 1.473c1.79-.328 3.657.223 4.938 1.64 1.28 1.417 1.634 3.32 1.03 5.038a.75.75 0 0 0 1.404.518c.77-2.127.324-4.543-1.198-6.216z"/>
            </svg>
          </a>
          <a href="#" class="text-gray-400 hover:text-white transition-colors duration-200">
            <span class="sr-only">LinkedIn</span>
            <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
              <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
            </svg>
          </a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup lang="ts">
const quickLinks = [
  { name: '首页', path: '/' },
  { name: '关于我们', path: '/about' },
  { name: '服务', path: '/services' },
  { name: '案例', path: '/cases' },
  { name: '联系我们', path: '/contact' },
]

const services = [
  '数字化转型咨询',
  '云计算解决方案',
  '人工智能应用',
  '数据分析服务',
  '移动应用开发',
]
</script>
