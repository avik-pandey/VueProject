<script>
  import modal from './components/modal.vue';


  export default {
    name: 'app',
    components: {
      modal,
      
    },
    data () {
      return {
        isModalVisible: false,
      };
    },
    methods: {
      showModal() {
        this.isModalVisible = true;
      },
      closeModal() {
        this.isModalVisible = false;
      }
    },
  };
</script>

<template>
  <div id="app">
    <button
      type="button"
      class="btn"
      @click="showModal"
    >
      Open Modal!
    </button>

    <modal
      v-show="isModalVisible"
      @close="closeModal"
    />
  </div>
</template>
<style  >
@media screen and (min-width: 480px) {
  .btn{
    position: relative;
   text-align:center;
   background: #4aae9b;
  }
}
</style>