<script setup lang="ts">
const features = [
  {
    number: '15+',
    title: '年行业经验',
    description: '多年专注宠物服务领域',
  },
  {
    number: '1000+',
    title: '满意客户',
    description: '服务超过千个宠物家庭',
  },
  {
    number: '50+',
    title: '专业团队',
    description: '资深兽医和美容师团队',
  },
  {
    number: '99%',
    title: '好评率',
    description: '客户满意度高达99%',
  },
]
</script>

<template>
  <section id="about" class="py-16 md:py-24 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid md:grid-cols-2 gap-12 items-center">
        <div class="relative">
          <div class="relative">
            <img
              src="/images/about-vet.png"
              alt="专业兽医"
              class="w-full h-80 object-cover rounded-2xl shadow-xl"
            />
            <div class="absolute -bottom-6 -right-6 bg-primary text-white p-6 rounded-2xl shadow-xl">
              <div class="text-4xl font-bold">15</div>
              <div class="text-sm opacity-80">年专业服务</div>
            </div>
          </div>
          <div class="absolute -top-4 -left-4 w-24 h-24 bg-orange-100 rounded-full -z-10"></div>
        </div>
        
        <div>
          <span class="inline-block bg-primary/10 text-primary px-4 py-1 rounded-full text-sm font-medium mb-4">
            关于我们
          </span>
          <h2 class="text-3xl md:text-4xl font-bold text-text mb-6">
            用爱陪伴每一个毛孩子
          </h2>
          <p class="text-text-light mb-6">
            宠物乐园成立于2010年，是一家集宠物医疗、美容、训练、寄养和领养于一体的综合性宠物服务机构。我们拥有专业的兽医团队、资深的美容师和训练师，致力于为每一位宠物提供最优质的服务。
          </p>
          <p class="text-text-light mb-8">
            我们坚信，每一个宠物都是家庭的一员，都值得被爱和呵护。我们的使命是让每一个毛孩子都能健康快乐地成长，让每一位宠物主人都能放心地将他们的宝贝交给我们。
          </p>
          
          <div class="grid grid-cols-2 gap-6">
            <div
              v-for="(feature, index) in features"
              :key="index"
              class="bg-gray-50 rounded-xl p-4"
            >
              <div class="text-2xl font-bold text-primary mb-1">{{ feature.number }}</div>
              <div class="font-semibold text-text mb-1">{{ feature.title }}</div>
              <div class="text-text-light text-sm">{{ feature.description }}</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
