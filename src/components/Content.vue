<template>
    <div class="content">
        <div class="img">
            <img src="../assets/product-img.jpg" alt="">
        </div>
        <div class="product-details">
            <h1>Product Title</h1>
            <p>Product Description Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ducimus perferendis distinctio facilis commodi culpa iste nulla id reiciendis aut dolorum? Autem laborum adipisci rerum dolor repellendus, modi nostrum eum voluptate.</p>
            <span>$100</span>
            <div class="product-button">
            <button class="add-basket" @click="openModalWithPortal">
                Portal
            </button>
            <button class="add-basket" @click="openModal">
                Not Portal
            </button>
            </div> 
        </div>
        <Modal productName="Blend Coffee" openModal="openModal" :show="show" @close="close"/>

        <div class="portal-modal">
            <portal to="basket">
                <Modal productName="Blend Coffee with Portal" openModalWithPortal="openModalWithPortal" :showPortal="showPortal" @close="closePortal"/>
            </portal>
        </div>
    </div>
</template>
<script>
import Modal from './Modal.vue'
export default {
   name: 'Content',
   components: {
      Modal
  },
  data() {
    return {
      show: false,
      showPortal: false
    }
  },
  methods: {
      openModalWithPortal(){
          this.showPortal = true
      },
      openModal(){
          this.show = true
      },
      close(){
          this.show = false
      },
      closePortal(){
          this.showPortal = false
      }
  }
}
</script>

<style scoped>
.content {
    margin-top: 2rem;
    padding: 2rem;
    border: 1px solid red;
    display: flex;
    position: absolute;
}
.product-details {
    padding-left: 3rem;
}
.content img {
    width: 300px;
    height: 300px;
}
.add-basket {
    margin-top: 1rem; 
    margin-right: 0.5rem;
    font-size: 16px;
}
</style>