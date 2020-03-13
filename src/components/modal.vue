<script>

import top from './header.vue';
import foot from './footer.vue';

export default {
  name: "modal",
   components: {
   
      top,
      foot
    }
 
};
</script>

<template>
  <transition name="modal-fade">
    <div class="modal-backdrop">
      <div
        class="modal"
        role="dialog"
        aria-labelledby="modalTitle"
        aria-describedby="modalDescription"
      >
        <top @close="$emit('close')"/>
        <section class="modal-body" id="modalDescription">
          <slot name="body"> Body!</slot>
        </section>
        <foot @close="$emit('close')"/>
      </div>
    </div>
  </transition>
</template>

<style>
.modal-backdrop {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: rgba(0, 0, 0, 0.3);
  display: flex;
  justify-content: center;
  align-items: center;
}

.modal {
  background: #ffffff;
  box-shadow: 2px 2px 20px 1px;
  overflow-x: auto;
  display: flex;
  flex-direction: column;
}

.modal-body {
  position: relative;
  padding: 20px 10px;
}
</style>