<template>
  <div :class="[
    'w-screen h-screen',
    'p-5',
  ]">
    <RabbitButton class="w-40" text="open" color="yellow"     
      @click="showed = true">
    </RabbitButton>
    <Modal title="嗨" :showModal="showed" @closing="showed = false">
      <template v-slot:itemText  >
        你好
      </template>
    </Modal>
  </div>
</template>

<script>
import Modal from './components/Modal.vue';
import RabbitButton from './components/RabbitButton.vue'

export default {
  data() {
    return {
      showed: true,
    }
  },
  components: {
    Modal,
    RabbitButton
  }
};
</script>
