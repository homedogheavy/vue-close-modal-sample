<template>
  <div>
    <button @click="showModal">show</button>
    {{show}}
    <modal v-if="show" :closeModal="closeModal"/>
  </div>
</template>

<script>
import Modal from './Modal.vue'

export default {
  name: 'CloseModal',
  methods: {
    showModal() {
      this.show = true
    },
    closeModal() {
      this.show = false
    }
  },
  components: {
    Modal
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
