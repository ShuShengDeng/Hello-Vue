<script setup lang="ts">
</script>

<template>
  <section id="home" class="bg-gradient-to-br from-background to-orange-100 py-16 md:py-24">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid md:grid-cols-2 gap-12 items-center">
        <div class="text-center md:text-left">
          <span class="inline-block bg-primary/10 text-primary px-4 py-1 rounded-full text-sm font-medium mb-4">
            宠物爱好者的乐园
          </span>
          <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-text leading-tight mb-6">
            给你的宠物
            <span class="text-primary">最好的爱</span>
          </h1>
          <p class="text-text-light text-lg mb-8 max-w-xl mx-auto md:mx-0">
            我们提供专业的宠物护理、美容、训练和领养服务，让每一个毛孩子都能健康快乐地成长。
          </p>
          <div class="flex flex-col sm:flex-row gap-4 justify-center md:justify-start">
            <button class="bg-primary hover:bg-primary-focus text-white px-8 py-3 rounded-full font-medium transition-colors shadow-lg hover:shadow-xl">
              了解更多
            </button>
            <button class="border-2 border-primary text-primary hover:bg-primary hover:text-white px-8 py-3 rounded-full font-medium transition-colors">
              预约服务
            </button>
          </div>
          <div class="mt-10 flex items-center gap-8 justify-center md:justify-start">
            <div class="text-center">
              <div class="text-3xl font-bold text-primary">1000+</div>
              <div class="text-text-light text-sm">满意客户</div>
            </div>
            <div class="w-px h-12 bg-gray-300"></div>
            <div class="text-center">
              <div class="text-3xl font-bold text-primary">50+</div>
              <div class="text-text-light text-sm">专业服务</div>
            </div>
            <div class="w-px h-12 bg-gray-300"></div>
            <div class="text-center">
              <div class="text-3xl font-bold text-primary">15年</div>
              <div class="text-text-light text-sm">行业经验</div>
            </div>
          </div>
        </div>
        <div class="relative">
          <div class="relative w-full aspect-square max-w-lg mx-auto">
            <div class="absolute inset-0 bg-primary/20 rounded-full blur-3xl"></div>
            <img
              src="/images/hero-golden-retriever.png"
              alt="可爱的金毛犬"
              class="relative z-10 w-full h-full object-cover rounded-3xl shadow-2xl"
            />
            <div class="absolute -bottom-4 -right-4 bg-white rounded-2xl p-4 shadow-xl z-20">
              <div class="flex items-center gap-3">
                <div class="w-12 h-12 bg-green-100 rounded-full flex items-center justify-center">
                  <svg class="w-6 h-6 text-green-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"/>
                  </svg>
                </div>
                <div>
                  <div class="font-semibold text-text">100%健康保障</div>
                  <div class="text-text-light text-sm">所有宠物经过严格体检</div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
