<script setup lang="ts">
const route = useRoute()
const page = ref(5)
function to(page: number) {
  return {
    query: {
      page
    },
  }
}
</script>

<template>
  <div class="container mx-auto p-4 box-border flex flex-row justify-center">
    <UPagination :to="to" v-model:page="page" :total="100" />
  </div>
</template>
