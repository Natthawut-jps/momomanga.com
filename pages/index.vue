<script setup lang="ts">

const page = ref(5);
function to(page: number) {
  return {
    query: {
      page,
    },
  };
}
</script>
<template>
  <div class="p-4 box-border">
    <p class="tezt-lg">มังงะสุดฮิต - {{ page }}</p>
    <div class="grid grid-cols-6 gap-4">
      <div class="col-span-6 md:col-span-4">
        <div
          class="py-4 box-border grid grid-cols-2 sm:grid-cols-4 lg:grid-cols-5 gap-2"
        >
          <div v-for="(item, index) in 20" :key="index">
            <div>
              <div>
                <NuxtImg
                  class="w-full object-cover"
                  src="/img/360297.jpg"
                  alt=""
                />
              </div>
              <div>title</div>
            </div>
          </div>
        </div>
        <div
          class="pt-4 px-4 box-border flex flex-row justify-center items-center"
        >
          <UPagination
            size="sm"
            v-model:page="page"
            :items-per-page="20"
            show-edges
            :sibling-count="1"
            :to="to"
            :total="100"
            active-color="neutral"
            active-variant="subtle"
            :ui="{ first: 'hidden', last: 'hidden' }"
          />
        </div>
      </div>
      <div class="rounded-md col-span-2 border-[1px] border-solid"></div>
    </div>
  </div>
</template>
