<template>
    <div class="modal" v-if="show || showPortal">
        <h1>{{ productName }}</h1>
        <button @click="$emit('close')">&times;</button>
    </div>
</template>
<script>
export default {
   name: 'Modal',
   props: {
    productName: {
      type: String,
      default: "Product Name Example"
    },
    show: {
      type: Boolean,
      default: false
    },
    showPortal: {
      type: Boolean,
      default: false
    }
   },
}
</script>
<style scope>
.modal{
  width: 300px;
  border: 1px solid #e6e6e6;
  z-index: 999;
  background-color: #fff;
  box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
  border-radius: 4px;
  overflow: hidden;
  padding: 2rem;
  position: fixed;
  display: flex;
  justify-content: space-between;

}
.modal button {
  width: 1.5rem;
  height: 1.5rem;
}
</style>