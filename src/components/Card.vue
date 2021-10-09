<script>
export default {
  name: "Card",
  props: ['path','board'],
  data(){
    return {
      hover: false
    }
  }
}
</script>

<template>
  <div @mouseover="hover = true" @mouseleave="hover = false" class="relative">
    <img :src="path" alt="" class="rounded-lg">
    <div v-if="hover" class="absolute bg-dark opacity-50 inset-0 w-full h-full rounded-lg"></div>
    <div v-if="hover" class="absolute top-0 w-full h-full flex flex-col justify-between p-3">
      <div class="flex items-center justify-between">
        <button class="flex items-center">
          <span class="font-semibold text-white">{{ board }}</span>
          <svg class="fill-current text-3xl text-white " height="12" width="12" viewBox="0 0 24 24" aria-hidden="true"
               aria-label="" role="img">
            <path
                d="M12 19.5.66 8.29c-.88-.86-.88-2.27 0-3.14.88-.87 2.3-.87 3.18 0L12 13.21l8.16-8.06c.88-.87 2.3-.87 3.18 0 .88.87.88 2.28 0 3.14L12 19.5z"></path>
          </svg>
        </button>
        <button class="rounded-full p-3 text-white bg-primary font-semibold">
          Save
        </button>
      </div>
      <div class="flex items-center w-full">
        <button class="ml-auto mr-2 bg-white rounded-full p-2 text-dark w-8 h-8 flex items-center justify-center opacity-80 hover:opacity:100">
          <svg class="text-base" height="16" width="16" viewBox="0 0 24 24" aria-hidden="true" aria-label="" role="img"><path d="M21 14c1.1 0 2 .9 2 2v6c0 1.1-.9 2-2 2H3c-1.1 0-2-.9-2-2v-6c0-1.1.9-2 2-2s2 .9 2 2v4h14v-4c0-1.1.9-2 2-2zM8.82 8.84c-.78.78-2.05.79-2.83 0-.78-.78-.79-2.04-.01-2.82L11.99 0l6.02 6.01c.78.78.79 2.05.01 2.83-.78.78-2.05.79-2.83 0l-1.2-1.19v6.18a2 2 0 1 1-4 0V7.66L8.82 8.84z"></path></svg>
        </button>
        <button class="bg-white rounded-full w-8 h-8 flex items-center justify-center text-dark opacity-80 hover:opacity:100">
          <svg class="text-base" height="16" width="16" viewBox="0 0 24 24" aria-hidden="true" aria-label="" role="img"><path d="M12 9c-1.66 0-3 1.34-3 3s1.34 3 3 3 3-1.34 3-3-1.34-3-3-3M3 9c1.66 0 3 1.34 3 3s-1.34 3-3 3-3-1.34-3-3 1.34-3 3-3zm18 0c1.66 0 3 1.34 3 3s-1.34 3-3 3-3-1.34-3-3 1.34-3 3-3z"></path></svg>
        </button>
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>