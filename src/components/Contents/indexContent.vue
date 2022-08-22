<template>
  <div class="block index-content-container">
  <MainSlider/>

  <GridCategory/>

  <FloatingBasket/>
  </div>
</template>

<script>
import MainSlider from "@/components/Contents/MainSlider";
import GridCategory from "@/components/Contents/GridCategory";
import FloatingBasket from "@/components/Contents/FloatingBasket";


export default {
  name: "indexContent",
  data() {
    return {
      mainDiscount: '20% تخفیف جوجه چینی با سس تارتار'
    }
  },
  components: {
    MainSlider,
    GridCategory,
    FloatingBasket
  },
}
</script>