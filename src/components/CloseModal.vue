<template>
  <div>
    <button @click="showModal">show</button>
    {{show}}
    <modal v-if="show" :show="show" :closeModal="closeModal"/>
  </div>
</template>

<script>
import Modal from './Modal.vue'

export default {
  name: 'CloseModal',
  data() {
    return {
      show: false
    }
  },
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
