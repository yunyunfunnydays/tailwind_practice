<template>
   <div class="border flex flex-col rounded-md overflow-hidden">
    <div class="p-3 border-b bg-blue-600 text-white font-bold flex justify-center items-center">
      2021 9 月
    </div>
    <div class="grid grid-cols-7 place-items-center">
      <div class="w-9 h-10 text-xs font-bold flex justify-center items-center" v-for="wd in weekDays" :key="wd">
        {{ wd }}
      </div>
    </div>
    <div class="grid grid-cols-7 place-items-center">
      <div class="w-9 h-10 text-sm flex justify-center items-center" v-for="d in 30" :key="d">
        {{ d }}
      </div>
    </div>
   </div>
</template>

<script>
export default {
  name:'SimpleCalendar',
  data() {
    return {
      weekDays: ['Su','Mo','Tu','We','Th','Fr','Sa']
    }
  },
}
</script>