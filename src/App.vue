<template>
  <div class="page p-8">
    <button
      type="button"
      @click="showModal = !showModal"
      class="mx-auto w-full flex justify-center rounded-md border border-gray-300 shadow-sm px-4 py-2 bg-white text-base font-medium text-gray-700 hover:bg-gray-50 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500 sm:mt-0 sm:ml-3 sm:w-auto sm:text-sm"
    >
      Open Modal
    </button>
    <ModalDialog :show="showModal" @close="showModal = false">
      <p class="mb-4">Gokuu is...</p>
      <img src="https://i.gifer.com/QjMQ.gif" />
    </ModalDialog>
  </div>
</template>

<script>
import ModalDialog from './components/ModalDialog.vue';
import { ref } from 'vue';

const components = {
  ModalDialog,
};
export default {
  name: 'App',
  components,
  setup() {
    const showModal = ref(false);
    return {
      showModal,
    };
  },
};
</script>

<style></style>
