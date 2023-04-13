<template>
  <div class="fixed top-0 left-0 w-screen h-screen p-5 flex justify-center items-center">
  <!-- Modal-Overlay -->
  <div class="absolute top-0 left-0 w-full h-full bg-black/50" />

  <!-- Modal-Window -->
  <div class="w-full max-w-sm bg-white rounded-md overflow-hidden z-10">
    <div class="p-3 border-b-2 flex justify-between items-center">
      <div class="font-bold text-gray-700">注意</div>
      <div class="">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-full w-full" fill="none" viewBox="0 0 24 24" stroke="currentColor"></svg>
      </div>
    </div>
  </div>
</div>
</template>

<script>
  export default {
    name: "Modal",
  }
</script>