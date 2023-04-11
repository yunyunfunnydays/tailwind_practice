<template>
   <div class="border flex flex-col rounded-md overflow-hidden">
    <div class="p-3 border-b bg-blue-600 text-white font-bold flex justify-center items-center ">
      {{year}} {{ month }} 月
    </div>
    <div class="grid grid-cols-7 place-items-center">
      <div class="w-9 h-10 text-xs font-bold flex justify-center items-center" v-for="wd in weekDays" :key="wd">
        {{ wd }}
      </div>
    </div>
    <div class="grid grid-cols-7 place-items-center">
      <div class="w-10 h-10 text-sm flex justify-center items-center" v-for="d in lastMonth" :key="d">
        {{ d }}
      </div>
      <div :class="['w-10 h-10',
       'text-sm flex justify-center items-center',
       ]"
        v-for=" d in thisMonth" :key="d">
        {{ d }}
      </div>
      <div class="w-10 h-10 text-sm flex justify-center items-center" v-for="d in nextMonth" :key="d">
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
      weekDays: ['Su','Mo','Tu','We','Th','Fr','Sa'],
      year: 2021,
      month: 9,
      today: new Date(),
    }
  },
  computed : {
    lastMonth() {
      const days = [];

      const currentDate = new Date(this.year, this.month - 1, 1);
      const wd = currentDate.getDay();

      for (let i = wd; i > 0; i--) {
        const temp = new Date(currentDate);
        temp.setDate(currentDate.getDate() - i);
        days.push(temp.getDate());
      }

      return days;
    },
    thisMonth() {
      const days = [];
      const current = new Date(this.year, this.month,0);
      for (let i = 1; i <= current.getDate(); i++) {
        days.push(i);
      }
      return days;
    },
    nextMonth() {
      const count = 42 - this.lastMonth.length -this.thisMonth.length;

      const days = [];

      for (let i = 1; i <= count; i++) {
        days.push(i);
      }
      return days;
    }
  }
}
</script>