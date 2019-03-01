<template>
  <div class="overlay"v-if="show" @click="closeModal">
    <div class="content">
      {{show}}
      <button @click="closeModal">close</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Modal',
  props: {
    show: Boolean,
    closeModal: Function
  },
  created() {
    document.addEventListener('keyup', this.close)
  },
  destroyed() {
    document.removeEventListener('keyup', this.close)
  },
  methods: {
    close(e) {
      if (e.code === 'Escape') {
        this.closeModal()
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.overlay {
  position: fixed;
  top: 0;
  left: 0;
  background: rgba(0,0,0, .5);
  z-index:10;
  height:100%;
  width: 100%
}
.content {
  background: white;
  width: 100px;
  height: 100px;
  position: relative;
  left: 43%;
  top: 43%;
}
</style>
