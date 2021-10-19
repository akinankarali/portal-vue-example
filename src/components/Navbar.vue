<template>
  <header class="header">
    <div class="header-inner">
        <h1 class="logo">PortalVue</h1>
       <div class="basket">
           <img src="../assets/shopping-cart.png" alt="">
        </div>
    </div>
  </header>
</template>

<script>
export default {

}
</script>

<style scoped>
.header-inner {
    margin-top: 20px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    border: 1px solid green;
    padding-left: 2rem;
    padding-right: 2rem;
}
.basket img {
    height: 24px;
    width: 24px;
}
</style>