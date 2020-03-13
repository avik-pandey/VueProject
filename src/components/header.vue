<script>
export default {
  name: "top",
   methods: {
    closeModal() {
      this.$emit("close");
    }
  }
};
</script>
<template>
  <header class="modal-header" id="modalTitle">
    <slot name="header">
      Title!
      <button
        type="button"
        class="btn-close"
        @click="closeModal"
        aria-label="Close modal"
      >x</button>
    </slot>
  </header>
</template>

<style>
.modal-header,
.modal-footer {
  padding: 15px;
  display: flex;
}

.modal-header {
  border-bottom: 1px solid #eeeeee;
  color: #4aae9b;
  justify-content: space-between;
}

.btn-close {
  border: none;
  font-size: 20px;
  padding: 20px;
  cursor: pointer;
  font-weight: bold;
  color: #4aae9b;
  background: transparent;
}
</style>

