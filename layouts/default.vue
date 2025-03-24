<template>
  <div>
    <header class="p-4 box-border flex flex-row items-center md:gap-16 shadow-md drop-shadow-md shadow-gray-800">
      <div class="md:flex-none flex-1">
        <img
          class="object-cover w-full max-w-[100px]"
          src="/img/Logo_momo-manga.png"
          alt=""
        />
      </div>
      <div class="hidden md:flex flex-row gap-8 items-end">
        <div class="min-w-fit"><a href="#">หน้าแรก</a></div>
        <div><a href="#">manga</a></div>
        <div><a href="#">manhwa</a></div>
        <div><a href="#">manhua</a></div>
      </div>
      <div class="md:flex-1 md:inline-block flex flex-row items-center gap-4">
        <div class="flex flex-row gap-2 items-end">
          <div
            class="hidden md:inline-block  py-1 px-2 md:p-0 bg-black/20 md:bg-transparent rounded-full cursor-pointer md:cursor-default"
          >
            <UIcon name="i-fa-solid-search" class="opacity-60" />
          </div>
          <UModal>
            <div
              class="inline-block md:hidden py-1 px-2 md:p-0 bg-black/20 md:bg-transparent rounded-full cursor-pointer md:cursor-default"
            >
              <UIcon name="i-fa-solid-search" class="opacity-60" />
            </div>
            <template #body>
              <div class="flex flex-row gap-2 items-center">
                <UIcon name="i-fa-solid-search" class="opacity-60" />
                <input
                  type="text"
                  placeholder="ค้นหา..."
                  class="w-full border-b border-solid border-amber-50/10 focus:outline-none text-gray-400 text-base"
                />
              </div>
            </template>
          </UModal>
          <input
            type="text"
            placeholder="ค้นหา..."
            class="w-full text-base max-w-[350px] border-b border-solid border-amber-50/10 md:block hidden focus:outline-none text-gray-400"
          />
        </div>
        <div class="inline-block md:hidden">
          <USlideover title="momomanga.com" side="left">
            <UButton
              color="neutral"
              class="cursor-pointer"
              variant="outline"
              icon="i-lucide-menu"
            />
            <template #body>
              <div class="flex flex-col gap-3">
                <div><a href="#">หน้าแรก</a></div>
                <div><a href="#">manga</a></div>
                <div><a href="#">manhwa</a></div>
                <div><a href="#">manhua</a></div>
              </div>
            </template>
          </USlideover>
        </div>
      </div>
    </header>
    <slot />
  </div>
  <footer class="bg-amber-600">footer</footer>
</template>
