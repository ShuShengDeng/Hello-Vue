<script setup lang="ts">
import { ref } from 'vue'

const form = ref({
  name: '',
  phone: '',
  email: '',
  message: '',
})

const handleSubmit = () => {
  alert('感谢您的留言，我们会尽快与您联系！')
  form.value = { name: '', phone: '', email: '', message: '' }
}
</script>

<template>
  <section id="contact" class="py-16 md:py-24 bg-gradient-to-br from-background to-orange-100">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-12">
        <span class="inline-block bg-primary/10 text-primary px-4 py-1 rounded-full text-sm font-medium mb-4">
          联系我们
        </span>
        <h2 class="text-3xl md:text-4xl font-bold text-text mb-4">
          与我们取得联系
        </h2>
        <p class="text-text-light max-w-2xl mx-auto">
          如有任何问题或需求，欢迎随时联系我们，我们将竭诚为您服务
        </p>
      </div>
      
      <div class="grid md:grid-cols-2 gap-12">
        <div class="bg-white rounded-2xl p-8 shadow-xl">
          <h3 class="text-2xl font-bold text-text mb-6">发送消息</h3>
          <form @submit.prevent="handleSubmit" class="space-y-4">
            <div>
              <label class="block text-text font-medium mb-2">姓名</label>
              <input
                v-model="form.name"
                type="text"
                required
                class="w-full px-4 py-3 border border-gray-300 rounded-xl focus:outline-none focus:ring-2 focus:ring-primary/50 focus:border-primary transition-colors"
                placeholder="请输入您的姓名"
              />
            </div>
            <div class="grid grid-cols-2 gap-4">
              <div>
                <label class="block text-text font-medium mb-2">电话</label>
                <input
                  v-model="form.phone"
                  type="tel"
                  required
                  class="w-full px-4 py-3 border border-gray-300 rounded-xl focus:outline-none focus:ring-2 focus:ring-primary/50 focus:border-primary transition-colors"
                  placeholder="请输入您的电话"
                />
              </div>
              <div>
                <label class="block text-text font-medium mb-2">邮箱</label>
                <input
                  v-model="form.email"
                  type="email"
                  class="w-full px-4 py-3 border border-gray-300 rounded-xl focus:outline-none focus:ring-2 focus:ring-primary/50 focus:border-primary transition-colors"
                  placeholder="请输入您的邮箱"
                />
              </div>
            </div>
            <div>
              <label class="block text-text font-medium mb-2">留言</label>
              <textarea
                v-model="form.message"
                rows="4"
                required
                class="w-full px-4 py-3 border border-gray-300 rounded-xl focus:outline-none focus:ring-2 focus:ring-primary/50 focus:border-primary transition-colors resize-none"
                placeholder="请输入您的留言"
              ></textarea>
            </div>
            <button
              type="submit"
              class="w-full bg-primary hover:bg-primary-focus text-white py-3 rounded-xl font-medium transition-colors"
            >
              发送消息
            </button>
          </form>
        </div>
        
        <div class="space-y-6">
          <div class="bg-white rounded-2xl p-6 shadow-lg">
            <div class="flex items-center gap-4">
              <div class="w-12 h-12 bg-primary/10 rounded-full flex items-center justify-center">
                <svg class="w-6 h-6 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"/>
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"/>
                </svg>
              </div>
              <div>
                <h4 class="font-semibold text-text">地址</h4>
                <p class="text-text-light">北京市朝阳区宠物大街123号</p>
              </div>
            </div>
          </div>
          
          <div class="bg-white rounded-2xl p-6 shadow-lg">
            <div class="flex items-center gap-4">
              <div class="w-12 h-12 bg-primary/10 rounded-full flex items-center justify-center">
                <svg class="w-6 h-6 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"/>
                </svg>
              </div>
              <div>
                <h4 class="font-semibold text-text">电话</h4>
                <p class="text-text-light">400-888-8888</p>
              </div>
            </div>
          </div>
          
          <div class="bg-white rounded-2xl p-6 shadow-lg">
            <div class="flex items-center gap-4">
              <div class="w-12 h-12 bg-primary/10 rounded-full flex items-center justify-center">
                <svg class="w-6 h-6 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/>
                </svg>
              </div>
              <div>
                <h4 class="font-semibold text-text">邮箱</h4>
                <p class="text-text-light">contact@petparadise.com</p>
              </div>
            </div>
          </div>
          
          <div class="bg-white rounded-2xl p-6 shadow-lg">
            <div class="flex items-center gap-4">
              <div class="w-12 h-12 bg-primary/10 rounded-full flex items-center justify-center">
                <svg class="w-6 h-6 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"/>
                </svg>
              </div>
              <div>
                <h4 class="font-semibold text-text">营业时间</h4>
                <p class="text-text-light">周一至周日 9:00-21:00</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
