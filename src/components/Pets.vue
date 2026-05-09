<script setup lang="ts">
const pets = [
  {
    name: '小金',
    type: '金毛犬',
    age: '3个月',
    gender: '公',
    image: 'https://trae-api-cn.mchost.guru/api/ide/v1/text_to_image?prompt=adorable%20golden%20retriever%20puppy%20sitting%20cute%20pose%20professional%20pet%20photography%20white%20background&image_size=square',
    tags: ['活泼', '友善', '聪明'],
    available: true,
  },
  {
    name: '花花',
    type: '英短猫',
    age: '6个月',
    gender: '母',
    image: 'https://trae-api-cn.mchost.guru/api/ide/v1/text_to_image?prompt=cute%20british%20shorthair%20cat%20kitten%20fluffy%20gray%20professional%20pet%20photography%20white%20background&image_size=square',
    tags: ['安静', '黏人', '温顺'],
    available: true,
  },
  {
    name: '旺财',
    type: '泰迪犬',
    age: '1岁',
    gender: '公',
    image: 'https://trae-api-cn.mchost.guru/api/ide/v1/text_to_image?prompt=adorable%20teddy%20poodle%20dog%20cute%20curly%20hair%20professional%20pet%20photography%20white%20background&image_size=square',
    tags: ['聪明', '活泼', '小巧'],
    available: false,
  },
  {
    name: '橘子',
    type: '橘猫',
    age: '2岁',
    gender: '公',
    image: 'https://trae-api-cn.mchost.guru/api/ide/v1/text_to_image?prompt=chubby%20orange%20tabby%20cat%20cute%20lazy%20pose%20professional%20pet%20photography%20white%20background&image_size=square',
    tags: ['贪吃', '慵懒', '亲人'],
    available: true,
  },
  {
    name: '可乐',
    type: '哈士奇',
    age: '4个月',
    gender: '公',
    image: 'https://trae-api-cn.mchost.guru/api/ide/v1/text_to_image?prompt=playful%20husky%20puppy%20blue%20eyes%20fluffy%20professional%20pet%20photography%20white%20background&image_size=square',
    tags: ['调皮', '活泼', '友善'],
    available: true,
  },
  {
    name: '雪球',
    type: '萨摩耶',
    age: '5个月',
    gender: '母',
    image: 'https://trae-api-cn.mchost.guru/api/ide/v1/text_to_image?prompt=beautiful%20samoyed%20puppy%20white%20fluffy%20smiling%20professional%20pet%20photography%20white%20background&image_size=square',
    tags: ['爱笑', '友善', '活泼'],
    available: false,
  },
]
</script>

<template>
  <section id="pets" class="py-16 md:py-24 bg-gradient-to-br from-orange-50 to-amber-100">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-12">
        <span class="inline-block bg-primary/10 text-primary px-4 py-1 rounded-full text-sm font-medium mb-4">
          待领养宠物
        </span>
        <h2 class="text-3xl md:text-4xl font-bold text-text mb-4">
          寻找温暖的家
        </h2>
        <p class="text-text-light max-w-2xl mx-auto">
          这些可爱的毛孩子正在等待一个温暖的家，给它们一个机会，也给自己一份快乐
        </p>
      </div>
      
      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
        <div
          v-for="(pet, index) in pets"
          :key="index"
          class="bg-white rounded-2xl overflow-hidden shadow-lg hover:shadow-xl transition-all duration-300"
        >
          <div class="relative">
            <img
              :src="pet.image"
              :alt="pet.name"
              class="w-full h-64 object-cover"
            />
            <span
              :class="[
                'absolute top-4 right-4 px-3 py-1 rounded-full text-sm font-medium',
                pet.available ? 'bg-green-500 text-white' : 'bg-gray-400 text-white'
              ]"
            >
              {{ pet.available ? '可领养' : '已领养' }}
            </span>
          </div>
          <div class="p-6">
            <div class="flex items-center justify-between mb-2">
              <h3 class="text-xl font-semibold text-text">{{ pet.name }}</h3>
              <span class="text-text-light text-sm">{{ pet.gender }}</span>
            </div>
            <div class="text-text-light text-sm mb-4">
              {{ pet.type }} · {{ pet.age }}
            </div>
            <div class="flex flex-wrap gap-2 mb-4">
              <span
                v-for="tag in pet.tags"
                :key="tag"
                class="bg-orange-100 text-primary px-3 py-1 rounded-full text-sm"
              >
                {{ tag }}
              </span>
            </div>
            <button
              :class="[
                'w-full py-3 rounded-full font-medium transition-colors',
                pet.available
                  ? 'bg-primary hover:bg-primary-focus text-white'
                  : 'bg-gray-200 text-gray-400 cursor-not-allowed'
              ]"
              :disabled="!pet.available"
            >
              {{ pet.available ? '立即领养' : '已被领养' }}
            </button>
          </div>
        </div>
      </div>
      
      <div class="text-center mt-8">
        <button class="border-2 border-primary text-primary hover:bg-primary hover:text-white px-8 py-3 rounded-full font-medium transition-colors">
          查看更多宠物
        </button>
      </div>
    </div>
  </section>
</template>
