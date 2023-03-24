<template>
<div :class="[
  'w-screen h-screen',
  'flex flex-col',
  'items-center',
  'pt-5',
]">
<AccordionMenuItem></AccordionMenuItem>
</div>
</template>
<script>
import AccordionMenuItem from './components/AccordionMenuItem.vue';

export default {
  data() {
    return {

    }
  },
  components: {
    AccordionMenuItem
  }
}
</script>
<style></style>
