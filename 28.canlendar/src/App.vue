<template>
  <div :class="[
    'w-screen h-screen',
    'flex items-center',
    'justify-center item-center'
    ]
  ">
    <SimpleCalendar></SimpleCalendar>
  </div>
</template>

<script>
import SimpleCalendar from './components/SimpleCalendar.vue'

export default {
  data() {
    return {

    }
  },
  components: {
    SimpleCalendar,
  }
}


</script>

<style></style>
