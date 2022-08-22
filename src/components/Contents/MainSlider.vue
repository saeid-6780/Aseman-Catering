<template>
  <div class="block overflow-hidden shadow-xl  z-10 ml-1" dir="rtl">
    <div class="w-full block bg-white a-border-radius-20 main-sidebar py-16 text-center">
      <p class="text-center text-white rounded-md opacity-25 py-3 px-2 inline main-sidebar-text">{{mainDiscount}}</p>
    </div>
  </div>
</template>

<script>

export default {
  name: "MainSlider",
  data() {
    return {
      mainDiscount: '20% تخفیف جوجه چینی با سس تارتار'
    }
  },

}
</script>

<style>
.index-content-container{width: 80%;border-radius: 20px;display: flex;flex-direction: column;}
.a-border-radius-20{border-radius: 20px;}
.main-sidebar{background-image:url("@/assets/img/home/mainsidebar.jpg") ;background-size: cover;background-repeat: no-repeat;border: 10px solid #fff;}
.main-sidebar-text{background: rgba(0,0,0,0.5);}
</style>