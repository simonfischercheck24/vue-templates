<template>
  <div
    class="m-6 block w-1/4 p-6 bg-white border border-gray-200 rounded-lg shadow hover:bg-gray-100"
  >
    <header class="mb-2 text-2xl font-bold tracking-tight text-gray-900">
      <slot name="header"></slot>
    </header>
    <div class="font-normal text-gray-700 break-words">
      <slot name="content"></slot>
    </div>
  </div>
</template>
