<template>
  <div class="py-2 h-[80vh] flex flex-col">
    <h2 class="dark:text-zinc-200 text-xl text-zinc-900 font-bold mb-2 px-1">所有分类</h2>
    <ul class="overflow-y-scroll">
      <li
        v-for="(item, index) in categorys"
        :key="item.id"
        class="dark:text-zinc-300 active:dark:bg-zinc-900 text-lg text-zinc-900 px-1 py-1.5 duration-100 active:bg-zinc-100"
        @click="$emit('onItemClick', index)"
      >
        {{ item.name }}
      </li>
    </ul>
  </div>
</template>

<script setup>
defineProps({
  categorys: {
    type: Array,
    required: true
  }
})
</script>

<style lang="scss" scoped></style>
