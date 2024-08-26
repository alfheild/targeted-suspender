<script lang="ts" setup>
import { ref } from 'vue'

const isdialogOpen = ref(true)
const setIsDialogOpen = (value: boolean) => (isdialogOpen.value = value)
</script>
<template>
  <div v-if="isdialogOpen">
    <div class="mx-auto max-w-7xl md:px-0 lg:p-6">
      <div
        class="relative isolate overflow-hidden bg-gray-900 px-6 pt-16 shadow-2xl lg:rounded-3xl md:pt-24 md:h-full sm:h-[100vh] lg:flex lg:gap-x-20 lg:px-24 lg:pt-0">
        <div class="absolute z-20 top-0 inset-x-0 flex justify-center overflow-hidden pointer-events-none">
          <div class="w-[108rem] flex-none flex justify-end">
          </div>
        </div>
        <div class="mx-auto max-w-md text-center lg:py-12 lg:mx-0 lg:flex-auto lg:text-left">
          <div class="flex items-center justify-center space-x-4 my-4 mx-auto">
            <div class="text-3xl text-white">+</div>
            <div class="text-3xl text-white">+</div>
          </div>
          <h2 class="text-3xl font-bold tracking-tight text-white sm:text-4xl">
            This is a content script running Vue, TypeScript, and Tailwind.css.
          </h2>
          <p class="mt-6 text-lg leading-8 text-gray-300">
            Learn more about creating cross-browser extensions by
            <button @click="setIsDialogOpen(false)" class="underline hover:no-underline
            ">
              closing this hint
            </button>
            .
          </p>
        </div>
        <div class="relative mt-16 h-80 lg:mt-8">
        </div>
      </div>
    </div>
  </div>
  <div v-else>
    <div class="mx-auto p-6">
      <button @click="setIsDialogOpen(true)"
        class="bg-white rounded-md p-3 text-sm font-semibold text-gray-900 shadow-sm hover:bg-gray-100 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-white">
        🧩 Open content script hint <span aria-hidden="true">+</span>
      </button>
    </div>
  </div>
</template>
