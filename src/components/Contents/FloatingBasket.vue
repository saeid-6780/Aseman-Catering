<template>
<a class="fixed right-0 floating-basket-container py-2 pr-4 pl-4 z-50">
  <i class=""></i>
</a>
</template>

<script>
export default {
  name: "FloatingBasket"
}
</script>

<style >
.floating-basket-container{background-color: #497f7b;bottom: 4%;border-top-left-radius: 20px;border-bottom-left-radius: 20px;}
.floating-basket-container > i{background-image: url("@/assets/img/home/basket-i.png");display: block;background-size: cover;width: 32px;height: 28px;}
</style>