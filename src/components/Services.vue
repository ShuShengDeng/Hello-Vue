<script setup lang="ts">
const services = [
  {
    icon: '🐾',
    title: '宠物美容',
    description: '专业美容师为您的宠物提供全方位美容服务，包括洗澡、修剪、护理等。',
    price: '¥100起',
  },
  {
    icon: '🏥',
    title: '健康体检',
    description: '先进设备和专业兽医团队，为宠物提供全面的健康检查和疾病预防。',
    price: '¥150起',
  },
  {
    icon: '🎾',
    title: '宠物训练',
    description: '专业训练师一对一指导，帮助宠物养成良好习惯，提升服从性。',
    price: '¥200起',
  },
  {
    icon: '🏠',
    title: '宠物寄养',
    description: '温馨舒适的寄养环境，24小时专人看护，让您外出无忧。',
    price: '¥80/天',
  },
  {
    icon: '❤️',
    title: '宠物领养',
    description: '与多家救助站合作，为流浪宠物寻找温暖的家，传递爱心。',
    price: '免费',
  },
  {
    icon: '💊',
    title: '医疗服务',
    description: '提供疫苗接种、驱虫、疾病治疗等专业医疗服务，守护宠物健康。',
    price: '¥50起',
  },
]
</script>

<template>
  <section id="services" class="py-16 md:py-24 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-12">
        <span class="inline-block bg-primary/10 text-primary px-4 py-1 rounded-full text-sm font-medium mb-4">
          我们的服务
        </span>
        <h2 class="text-3xl md:text-4xl font-bold text-text mb-4">
          全方位宠物服务
        </h2>
        <p class="text-text-light max-w-2xl mx-auto">
          我们致力于为您的宠物提供最优质的服务，让它们健康快乐地成长
        </p>
      </div>
      
      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
        <div
          v-for="(service, index) in services"
          :key="index"
          class="bg-gray-50 rounded-2xl p-6 hover:shadow-xl transition-all duration-300 hover:-translate-y-1"
        >
          <div class="text-4xl mb-4">{{ service.icon }}</div>
          <h3 class="text-xl font-semibold text-text mb-2">{{ service.title }}</h3>
          <p class="text-text-light mb-4">{{ service.description }}</p>
          <div class="flex items-center justify-between">
            <span class="text-primary font-bold text-lg">{{ service.price }}</span>
            <button class="text-primary hover:text-primary-focus font-medium">
              了解详情 →
            </button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
