<template>
  <div :class="[
    'w-screen h-screen',
    'p-5',
    'bg-red-200'
  ]">
    b
    <Modal>
      
    </Modal>
  </div>
</template>

<script>
import Modal from './components/Modal.vue';

export default {
  data() {
    return {
    }
  },
  components: {
    Modal,
  }
};
</script>
