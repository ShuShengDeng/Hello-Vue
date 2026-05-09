<script setup lang="ts">
import { ref } from 'vue'

const isMenuOpen = ref(false)

const navItems = [
  { name: '首页', href: '#home' },
  { name: '服务', href: '#services' },
  { name: '宠物', href: '#pets' },
  { name: '关于我们', href: '#about' },
  { name: '联系我们', href: '#contact' },
]

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}
</script>

<template>
  <header class="bg-white shadow-lg sticky top-0 z-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between items-center h-16">
        <div class="flex items-center gap-2">
          <svg class="w-8 h-8 text-primary" fill="currentColor" viewBox="0 0 24 24">
            <path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm4.64 6.8c-.15 1.58-.8 5.42-1.13 7.19-.14.75-.42 1-.68 1.03-.58.05-1.02-.38-1.58-.75-.88-.58-1.38-.94-2.23-1.5-.99-.65-.35-1.01.22-1.59.15-.15 2.71-2.48 2.76-2.69a.2.2 0 00-.05-.18c-.06-.05-.14-.03-.21-.02-.09.02-1.49.95-4.22 2.79-.4.27-.76.41-1.08.4-.36-.01-1.04-.2-1.55-.37-.63-.2-1.12-.31-1.08-.66.02-.18.27-.36.74-.55 2.92-1.27 4.86-2.11 5.83-2.51 2.78-1.16 3.35-1.36 3.73-1.36.08 0 .27.02.39.12.1.08.13.19.14.27-.01.06.01.24 0 .38z"/>
          </svg>
          <span class="text-xl font-bold text-text">宠物乐园</span>
        </div>
        
        <nav class="hidden md:flex items-center gap-8">
          <a
            v-for="item in navItems"
            :key="item.name"
            :href="item.href"
            class="text-text-light hover:text-primary transition-colors font-medium"
          >
            {{ item.name }}
          </a>
        </nav>
        
        <div class="hidden md:block">
          <button class="bg-primary hover:bg-primary-focus text-white px-6 py-2 rounded-full font-medium transition-colors">
            立即领养
          </button>
        </div>
        
        <button
          class="md:hidden p-2 text-text-light hover:text-primary"
          @click="toggleMenu"
        >
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path v-if="!isMenuOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"/>
            <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"/>
          </svg>
        </button>
      </div>
      
      <div v-if="isMenuOpen" class="md:hidden py-4 border-t">
        <nav class="flex flex-col gap-4">
          <a
            v-for="item in navItems"
            :key="item.name"
            :href="item.href"
            class="text-text-light hover:text-primary transition-colors font-medium px-2"
            @click="isMenuOpen = false"
          >
            {{ item.name }}
          </a>
          <button class="bg-primary hover:bg-primary-focus text-white px-6 py-2 rounded-full font-medium transition-colors mt-2 mx-2">
            立即领养
          </button>
        </nav>
      </div>
    </div>
  </header>
</template>
