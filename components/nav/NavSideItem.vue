<script setup lang="ts">
defineProps<{
  text: string
  icon: string
  to: string
}>()
</script>

<template>
  <NuxtLink :to="to" active-class="text-primary" group focus:outline-none>
    <div flex w-fit px5 py2 gap2 items-center transition-100 rounded-full group-hover:bg-active group-focus-visible:ring="2 current">
      <slot name="icon">
        <div :class="icon" />
      </slot>
      <span>{{ text }}</span>
    </div>
  </NuxtLink>
</template>