<script>
export default {
  name: "foot",
   methods: {
    close() {
      this.$emit("close");
      console.log("ok");
    },
    closeModal() {
        this.isModalVisible = false;
      }
  }
};
</script>


<template>
  <footer class="modal-footer">
    <slot name="footer">
      I'm the default footer!
      <button
        type="button"
        class="btn-green"
        @click="closeModal"
        aria-label="Close modal"
      >Close me!</button>
    </slot>
  </footer>
</template>

<style >
.modal-header,
.modal-footer {
  padding: 15px;
  display: flex;
}

.modal-footer {
  border-top: 1px solid #eeeeee;
  justify-content: flex-end;
}

.btn-green {
  color: white;
  background: #4aae9b;
  border: 1px solid #4aae9b;
  border-radius: 2px;
}
</style>
