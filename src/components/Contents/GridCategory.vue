<template>
<div class="block overflow-hidden shadow-xl bg-white z-10 grid-category ml-1 mt-1 a-border-radius-20">
  <div class="flex text-center mx-auto">
    <h2 class="w-10/12 mx-auto text-center lined-title"><span>{{title}}</span></h2>
  </div>

  <div class="block" v-if="windowWidth<768">
    <div class="flex mb-6" v-for="index in ((cats.length)/2)" v-bind:key="index" >
      <div class="w-1/2 md:w-4/12 px-2 text-center">
        <img :src="cats[((index-1)*2)].img" alt="" class="a-border-radius-20">
        <h4 class="mt-1">{{ cats[((index-1)*2)].name }}</h4>
      </div>
      <div class="w-1/2 md:w-4/12 px-2 text-center">
        <img :src="cats[((index-1)*2)+1].img" alt="" class="a-border-radius-20">
        <h4 class="mt-1">{{ cats[((index-1)*2)+1].name }}</h4>
      </div>
    </div>

  </div>
  <div class="block" v-else>
    <div class="flex mb-6" v-for="index in ((cats.length)/3)" v-bind:key="index" >
      <div class="w-1/2 md:w-4/12 px-2 text-center">
        <img :src="cats[((index-1)*2)].img" alt="" class="a-border-radius-20">
        <h4 class="mt-1">{{ cats[((index-1)*2)].name }}</h4>
      </div>
      <div class="w-1/2 md:w-4/12 px-2 text-center">
        <img :src="cats[((index-1)*2)+1].img" alt="" class="a-border-radius-20">
        <h4 class="mt-1">{{ cats[((index-1)*2)+1].name }}</h4>
      </div>
      <div class="w-1/2 md:w-4/12 px-2 text-center">
        <img :src="cats[((index-1)*2)+1].img" alt="" class="a-border-radius-20">
        <h4 class="mt-1">{{ cats[((index-1)*2)+2].name }}</h4>
      </div>
    </div>

  </div>
</div>
</template>

<script>
export default {
  name: "GridCategory",
  data() {
    return {
      title: 'دسته بندی ها',

      cats: [
        {
          img: process.env.BASE_URL + 'img/home/cat-img.jpg',
          name: 'کباب',
        }, {
          img: process.env.BASE_URL + 'img/home/cat-img.jpg',
          name: 'خوراک ها',
        }, {
          img: process.env.BASE_URL + 'img/home/cat-img.jpg',
          name: 'خورش ها',
        }, {
          img: process.env.BASE_URL + 'img/home/cat-img.jpg',
          name: 'چلو و پلو',
        }, {
          img: process.env.BASE_URL + 'img/home/cat-img.jpg',
          name: 'اشتها آور سالاد',
        }, {
          img: process.env.BASE_URL + 'img/home/cat-img.jpg',
          name: 'نوشیدنی ها',
        }
      ],
      windowWidth: window.innerWidth
    }
  },
  computed: {
    on_mobile() {
      return false
    },
  },
  mounted() {
    this.$nextTick(() => {
      window.addEventListener('resize', this.onResize);
    })
  },

  beforeDestroy() {
    window.removeEventListener('resize', this.onResize);
  },

  methods: {
    onResize() {
      this.windowWidth = window.innerWidth
    }
  }
}
</script>

<style >
.lined-title{border-bottom: 2px solid #b89d50;line-height: 0.1em;margin: 25px 0 25px; }
.lined-title span {background:#fff;padding:0 10px;}
.grid-category{flex-grow: 1;}

</style>